# openHASP Gallery Content Store

Dieses Repository dient als reiner Content-Store fuer die oeffentliche openHASP-Design-Gallery.

## Struktur

```text
gallery/
  index.json
  designs/
    <design-id>/
      package.json
      preview.png
      assets/
        ...
```

## Bedeutung

- `gallery/index.json`
  Enthält den oeffentlichen Index aller freigegebenen Designs aus `main`.
- `gallery/designs/<design-id>/package.json`
  Enthält das sanitierte Gallery- oder Debug-Paket eines Designs.
- `gallery/designs/<design-id>/assets/`
  Enthält optionale, explizit freigegebene Assets fuer dieses Design.
- `gallery/designs/<design-id>/preview.png`
  Optionale Vorschau fuer Gallery-Listen.

## Moderation

- Neue Designs werden ueber Branches / Pull Requests vorbereitet.
- Nur Inhalte in `main` gelten als veroeffentlicht.
- Das eigentliche App-Frontend liest ausschliesslich freigegebene Inhalte aus `main`.

## Root-Datei

Die Root-Datei `index.json` verweist bewusst auf `gallery/index.json`, damit Clients mit einem festen Einstiegspunkt arbeiten koennen.
