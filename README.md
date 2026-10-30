# Hi, I'm Heliedan 👋

I run a self-hosted seedbox and my own network services (Swizzin, ruTorrent, Pi-hole, Unbound, DNS over HTTPS, WireGuard), and I use them every day, including on an iPad. When something breaks, I reproduce it, report it with exact steps, and send a small fix tested before and after.

## Merged contributions

- **ruTorrent:**
  - I translated the French interface strings that were still in English and fixed wrong translations ([#3458](https://github.com/Novik/ruTorrent/pull/3458)).
  - I fixed two plugins that showed the wrong startup error ([#3459](https://github.com/Novik/ruTorrent/pull/3459)).
  - Both are in ruTorrent 5.3.19.
  - A private torrent added with "Randomize info hashes" ticked now keeps its own info hash, so private trackers no longer refuse it as unregistered ([#3467](https://github.com/Novik/ruTorrent/pull/3467)).
  - The first line of the Log tab is now translated ([#3468](https://github.com/Novik/ruTorrent/pull/3468)).
  - In the File Manager plugin, "New Archive", "Copy" and "File Checksum" now work from the torrent Files tab ([#90](https://github.com/nelu/rutorrent-filemanager/pull/90)).
  - In the Telegram notification plugin proposed for ruTorrent, real notifications from rTorrent now arrive, custom templates no longer get refused by Telegram, and Telegram's error text is shown ([drrako/ruTorrent#2](https://github.com/drrako/ruTorrent/pull/2)).
  - Three iPad bugs I reported were fixed by the maintainers ([#3346](https://github.com/Novik/ruTorrent/pull/3346), [#3348](https://github.com/Novik/ruTorrent/pull/3348), [#3361](https://github.com/Novik/ruTorrent/pull/3361)).
- **docker-doh** (DNS over HTTPS server image):
  - an empty timeout or number of tries no longer stops the container ([#55](https://github.com/satishweb/docker-doh/pull/55));
  - `DOH_CONFIG_FILE` is no longer read as a Docker secret ([#56](https://github.com/satishweb/docker-doh/pull/56));
  - the health check reads the configuration file set by `DOH_CONFIG_FILE` ([#61](https://github.com/satishweb/docker-doh/pull/61)).
- **Suwayomi** (manga reader web interface): a search saved with filters in an older version no longer crashes the source page ([#1181](https://github.com/Suwayomi/Suwayomi-WebUI/pull/1181)).
- **Bazarr** (subtitle manager): "Remove HI" no longer deletes dialogue between two hearing impaired tags ([#3687](https://github.com/morpheus65535/bazarr/pull/3687)).
- **Unbound** (DNS resolver image by madnuttah): the images now include the DNSSEC root trust anchor, so `unbound-checkconf` works in a fresh container ([#242](https://github.com/madnuttah/unbound-docker/pull/242)).

Under review, among others: flood, cross-seed, mkbrr, Swizzin and its dashboard. [All my pull requests](https://github.com/search?q=author%3AHeliedan+is%3Apr&type=pullrequests).

## My project

**[My edition of the Swizzin dashboard](https://github.com/Heliedan/swizzin_dashboard)** (unofficial):
- an App Store to install and uninstall apps from the panel;
- live CPU, RAM and disk cards with a disk-full alert;
- login protection.

It is tested on Ubuntu 20.04 to 24.04 and Debian 11 and 12. Latest release: [heliedan-2.4](https://github.com/Heliedan/swizzin_dashboard/releases/tag/heliedan-2.4).

## How I work

I'm not a developer. Analysis and patches are prepared with the help of an AI assistant. Every bug is reproduced, and every fix is tested before and after, on my own server or in throwaway containers, before I send it.
