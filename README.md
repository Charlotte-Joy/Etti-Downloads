# Etti downloads

Installers for Etti apps, linked from [etti.com.au](https://etti.com.au). Buy and download from
the website; this repository only holds the files.

Each app has one release whose installer is replaced when a new version ships, so its download
link never changes:

| App | Download |
|---|---|
| Etti Awake (macOS) | https://github.com/Charlotte-Joy/Etti-Downloads/releases/download/awake/Etti-Awake.dmg |

Mac installers are signed with a Developer ID and notarised by Apple.

## Shipping a new version (for whoever maintains this)

```bash
gh release upload awake Etti-Awake.dmg --clobber -R Charlotte-Joy/Etti-Downloads
gh release edit awake --notes "Version <x.y.z>" -R Charlotte-Joy/Etti-Downloads
```

Check the file first with `spctl --assess --type open --context context:primary-signature -v Etti-Awake.dmg`
("Notarized Developer ID").
