# Ghostty config

Ma configuration macOS de [Ghostty](https://ghostty.org/) : thèmes adaptatifs **Codex Dark** et **Codex Light**, police **Dank Mono** en 14 pt, et réglages pensés pour les longues sorties d'agents dans le terminal.

## Contenu

- `config` : réglages Ghostty actifs ;
- `themes/Codex Dark` et `themes/Codex Light` : thèmes locaux sélectionnés automatiquement selon l'apparence de macOS ;
- `themes/Winter is Coming Dark Blue` : ancien thème conservé comme solution de repli.

## Installation

Sauvegardez votre configuration existante, puis installez les fichiers :

```zsh
mkdir -p ~/.config/ghostty/themes
cp "$HOME/Library/Application Support/com.mitchellh.ghostty/config.ghostty" \
  "$HOME/Library/Application Support/com.mitchellh.ghostty/config.ghostty.backup"
cp config "$HOME/Library/Application Support/com.mitchellh.ghostty/config.ghostty"
cp themes/Codex\ Dark themes/Codex\ Light ~/.config/ghostty/themes/
```

Installez aussi la police [Dank Mono](https://philpl.gumroad.com/l/dank-mono) avant de lancer Ghostty. Ouvrez ensuite une nouvelle fenêtre, ou rechargez la configuration avec `Cmd+Shift+,`.

## Vérification

```zsh
ghostty +show-config --changes-only
ghostty +list-themes --plain --path
```

Le résultat doit notamment afficher `theme = light:Codex Light,dark:Codex Dark`, `font-family = Dank Mono` et `font-size = 14`.

## Licence

Les réglages de ce dépôt sont disponibles sous licence [MIT](LICENSE). Les thèmes Codex reprennent les palettes `catppuccin-mocha` et `catppuccin-latte` utilisées comme valeurs adaptatives par [openai/codex](https://github.com/openai/codex). Le thème de repli est adapté de [johnpapa/vscode-winteriscoming](https://github.com/johnpapa/vscode-winteriscoming).
