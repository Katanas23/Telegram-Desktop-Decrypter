# Telegram Desktop Decrypter

This Python library provides a comprehensive solution for decrypting and parsing Telegram Desktop's local data files (tdata). It allows secure extraction of account information, settings, and authentication keys from Telegram's encrypted desktop storage.

## Features  

- Decrypting Telegram Desktop's local data files  
- View user ID, master data centre (DC) ID and verification keys  
- Reading application settings  
- Support encrypted and unencrypted data  
- Flexible key management  
- Compatibility with different Telegram Desktop versions  
- Ability to output in JSON format  
- Analyse and show encrypted settings (if available)

## Requirements

Python 3.8+
tgcrypto library
typing module
enum module

## Installation
- Type the command `pip install .` at the location where `setup.py` is located

## Usage

You can run it on the command line as follows:

```sh
python main.py <tdata_path> [--passcode <password>] [--show_settings] [--json]
```
`"C:\Users\YOURPCUSERNAME\AppData\Roaming\Telegram Desktop\tdata"`

### Parameters

- `<tdata_path>`: Path to the Telegram `tdata/` directory.
- `--passcode`, `-p`: (Optional) If `tdata/` is encrypted, a password must be entered.
- `-show_settings`: Shows the decoded Telegram settings.
- `--json`, `-j`: Allows you to get the output in JSON format.

#### Example Uses

**Get account information as standard output:**

```sh
python main.py /path/to/tdata/
```

**Getting account information in JSON format:**

```sh
python main.py /path/to/tdata/ --json
```

**Settings also show:**

```sh
python main.py /path/to/tdata/ --show_settings
```

**Read the encrypted `tdata/` directory:**

```sh
python main.py /path/to/tdata/ --passcode ‘sifre’
```

## Debugging

- If you get the error `No key file was found. Is the tdata path correct?’ error, check that the specified `tdata/` directory is correct.
- If you use an encrypted `tdata/`, be sure to include the `--passcode` parameter.


## Disclaimer

This tool is provided for educational and research purposes. Always respect privacy and legal guidelines.

## License

This project is licensed under the MIT License. Refer to the LICENSE file for more information.

