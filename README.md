# Ghostty config

Ma configuration macOS de [Ghostty](https://ghostty.org/) : thème **Winter is Coming Dark Blue**, police **Dank Mono** en 14 pt, et réglages pensés pour les longues sorties d'agents dans le terminal.

## Contenu

- `config` : réglages Ghostty actifs ;
- `themes/Winter is Coming Dark Blue` : thème local utilisé par la configuration.

## Installation

Sauvegardez votre configuration existante, puis installez les fichiers :

```zsh
mkdir -p ~/.config/ghostty/themes
cp "$HOME/Library/Application Support/com.mitchellh.ghostty/config.ghostty" \
  "$HOME/Library/Application Support/com.mitchellh.ghostty/config.ghostty.backup"
cp config "$HOME/Library/Application Support/com.mitchellh.ghostty/config.ghostty"
cp "themes/Winter is Coming Dark Blue" ~/.config/ghostty/themes/
```

Installez aussi la police [Dank Mono](https://philpl.gumroad.com/l/dank-mono) avant de lancer Ghostty. Ouvrez ensuite une nouvelle fenêtre, ou rechargez la configuration avec `Cmd+Shift+,`.

## Vérification

```zsh
ghostty +show-config --changes-only
ghostty +list-themes --plain --path
```

Le résultat doit notamment afficher `theme = Winter is Coming Dark Blue`, `font-family = Dank Mono` et `font-size = 14`.

## Licence

Les réglages de ce dépôt sont disponibles sous licence [MIT](LICENSE). Le thème est adapté de [johnpapa/vscode-winteriscoming](https://github.com/johnpapa/vscode-winteriscoming) ; ses éléments graphiques restent soumis à la licence de leur projet d'origine.
