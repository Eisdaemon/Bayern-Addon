# Bayern Add-On

Browser Extension, which replaces words like Koschi with Gamelle or Hopo with Topf

## 🛠 Installation

### Firefox (>= 51)
- download the repo
- open `about:debugging`
- click "Load Temporary Add-on"
- select any file in your extension's directory, e.g. `manifest.json`

### Chrome / Opera / Edge (>= 76)

- Not yet available

## ℹ️ Notice

Use browser extensions at your own risk.

Always reassure that the extension didn't edit any input fields or textareas in the browser, like Github or other sites where frontend editing is possible.

I'm not responsible for possible wrong submitted data or reduced rendering performance.

## 🔀 Contribution

Feel free to open pull requests with new names or persons.

When adding new persons follow this format of the object:

```javascript
{
    regexName: /(?:Vorname )?Nachname/gi, // looking for optional firstname, lastname not optional
    regexAbbrev: /VN/gi,
    substitutionsFirst: ["Vorname1"],
    substitutionsMiddle: ["Zwischenname1"],
    substitutionsLast: ["Nachname1"], // for hyphen "-" concatenated, names add those in front of the lastname
    substitutionsComplete: ["Spitzname1"],
  }
```
Afterwards, since i didn't bother with a settings file like the original, add in content.js a "person-id": "on", under settings_persons
Please don't submit stuff, that is out of the borders of satire.

## 🔨 Development

- first do: `npm install`
- for development in Firefox run `npm run start:firefox`
- the extension will reload if any source file changes
- Before submitting code:
  please use Prettier by using `npx prettier --write .`

## 👍 Credits

- Forked from https://github.com/viktorsec/bumpercar-candysnatch
- Later forked from https://github.com/voodoocode/pannengeraet-krank-knarrenbauer
