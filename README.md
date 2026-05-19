# QR Code Generator CLI

A simple command-line tool that asks for a URL and generates a QR code image for it.

## Requirements

- Node.js 14 or higher

## Installation

Clone the repo and install dependencies:

```bash
git clone https://github.com/ishaq0112/qr-code-generator
cd 
npm install
```

## Usage

Run the script:

```bash
node index.js
```

You'll be prompted to enter a URL:

```
? Enter your URL:  https://google.com
```

A `qrcode.png` file will be saved in the project folder. Open it, scan it with your phone camera, and it should take you straight to the URL you entered.

## How it works

- **[inquirer](https://www.npmjs.com/package/inquirer)** prompts the user in the terminal and returns their input.
- **[qr-image](https://www.npmjs.com/package/qr-image)** converts the URL into a QR code image stream.
- The QR stream is piped into `fs.createWriteStream` to save it as a PNG file.

## Dependencies

- `inquirer` — interactive command-line prompts
- `qr-image` — QR code generation
