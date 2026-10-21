# Borgerberedskab

A Danish/English citizen preparedness app with a restrained public-service design. Built with plain HTML, CSS and JavaScript. No packages or build step.

## Run

Open `index.html` directly in a browser, or serve the directory:

```sh
python -m http.server 8000
```

Then open http://localhost:8000.

## What it does

- Action plans for power, communications and payment disruptions, with separate preparation and incident views.
- A manually guided review of suspicious messages, without claiming to authenticate them.
- A household contact and meeting agreement saved on the device.
- A self-contained offline HTML export containing guidance and the saved agreement.
- A printable agreement, action plans and supplies list.
- Three decision exercises covering loss of contact, fraudulent requests and unconfirmed warnings.
- Household supply planning and water calculations.

The focus is handling the consequences of disruption and practising decisions. It does not identify hostile actors, infer sabotage from outages, issue warnings or replace emergency services. There is no live incident feed, threat score or automatic fact-checking.

## Data and offline use

Saved choices and agreements use localStorage, with no application server or account. Browser data can be cleared and is not synchronised across devices. Exported files may contain personal contact details. External source links and new official messages require internet. Save and open an offline copy before relying on it.

## Sources

The Sources page links to Beredskabsstyrelsen, Styrelsen for Samfundssikkerhed, Sikkerdigital and PET. This is an independent tool; current official instructions take priority.

## Validation

JavaScript syntax and static structure checked. Desktop and 390 px mobile layouts visually reviewed. Saved agreement persistence, language switching, message-review branches and the complete three-step exercise tested in the browser. Offline export generation checked; reopening a downloaded file in a fully disconnected browser remains a manual acceptance check.

## Visual design

The interface uses a navy navigation bar, neutral surfaces and a typographic wordmark rather than an invented authority crest. `styles.css` contains responsive layouts. The household overview shows actual stored selections, not a readiness score. Offline exports embed the stylesheet so the downloaded file remains self-contained.
