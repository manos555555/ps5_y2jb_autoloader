# PS5 Y2JB Autoloader

Fork of [Y2JB](https://github.com/Gezine/Y2JB)

Automatically loads the kernel exploit, elf_loader, your elf payloads, and .js scripts.

Supports PS5 firmwares 4.03-10.01

## How to Use

- Create a directory named `ps5_autoloader`.
- Inside this directory, place your `.elf`, `.bin`, and `.js` files, and an `autoload.txt` file.
  - In `autoload.txt`, list the files you want to load, one filename per line.
  - Filenames are case-sensitive — ensure each name exactly matches the file.
  - You can add lines like `!1000` to make the loader wait 1000 ms before sending the next payload.
  - Do NOT include the kernel exploit (e.g., `lapse.js`) or the elf_loader in `autoload.txt`; they are loaded automatically.
- Put the `ps5_autoloader` directory in one of these locations (priority order - highest first):
  - Root of a USB drive
  - Internal drive: `/data/ps5_autoloader`
  - The YT's splash_screen folder: `download0/cache/splash_screen/aHR0cHM6Ly93d3cueW91dHViZS5jb20vdHY=/ps5_autoloader`

## How to Update

Since version **v0.2**, you can update the autoloader by simply placing **`y2jb_update.zip`** (from the [Releases page](https://github.com/itsPLK/ps5_y2jb_autoloader/releases)) on the **root** of a USB drive, and starting the app.

## Setup Instructions

If you're jailbroken, you can setup it manually just like the original [Y2JB](https://github.com/Gezine/Y2JB/blob/main/README.md).  

## Credits

* **[Gezine](https://github.com/Gezine)** - creator of the original [Y2JB](https://github.com/Gezine/Y2JB)
* **[shahrilnet](https://github.com/shahrilnet), [null_ptr](https://github.com/n0llptr)** - Referenced many codes from [Remote Lua Loader](https://github.com/shahrilnet/remote_lua_loader)
* **[ntfargo](https://github.com/ntfargo)** - Thanks for providing V8 CVEs and CTF writeups
* **abc and psfree team** - Lapse implementation
* **[flat_z](https://github.com/flatz) and [LM](https://github.com/LightningMods)** - Helping implement GPU rw using direct ioctl
* **[john-tornblom](https://github.com/john-tornblom) and [EchoStretch](https://github.com/EchoStretch)** - Providing elfldr.elf payload
* **[hammer-83](https://github.com/hammer-83)** - Various BD-J PS5 exploit references
* **[zecoxao](https://github.com/zecoxao), [idlesauce](https://github.com/idlesauce), and [TheFlow](https://github.com/theofficialflow)** - Helping troubleshoot dlsym
* **[Dr.Yenyen](https://github.com/DrYenyen) and PS5 R&D community** - Testing Y2JB
* **Rush** - Creating Y2JB backup file

## Disclaimer

This tool is provided as-is for research and development purposes only. Use at your own risk. The developers are not responsible for any damage, data loss, or consequences resulting from the use of this software.
