# heyaudit-email-assets

Öffentlich ausgelieferte Bilder für HeyAudit-E-Mails, über jsDelivr:

```
https://cdn.jsdelivr.net/gh/TedOsa25/heyaudit-email-assets@main/<datei>
```

Warum ein eigenes Repository: Bilder in E-Mails müssen von einer öffentlich
erreichbaren URL kommen. Data-URIs zeigt Gmail nicht an, und Anhänge landen
im Spamfilter. Dasselbe Muster nutzt bereits `heycarbo-email-assets`.

Verdrahtet über `assets.hostedAssetBase` im Brand-Profil der Revenue Engine
(`ai-os/packages/tedos-engine/src/revenue/brand-profiles/heyaudit.ts`).

| Datei | Verwendung | Format |
|---|---|---|
| `mira-hansen.jpg` | Signaturbild, rund | 220 x 220, Kreis in die Datei eingebrannt |

Der Kreis steckt in der Datei und nicht in CSS, weil Outlook `border-radius`
auf `<img>` ignoriert und das Bild dort sonst quadratisch erscheint. Der Grund
ist deckend weiß, also genau die Kartenfarbe der Mail.
