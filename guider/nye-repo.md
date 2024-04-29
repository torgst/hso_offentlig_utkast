# Vil du ha repositories på GitHub?

Dette er en liten sjekkliste repositories må oppfylle for å være på GitHub.

## Lisens

Helse Sør-Øst har valgt MIT som standard lisens. Alle repos [må ha en `LICENSE`-fil](../LISENSIERING.md).

## Readme

Vi har en [standard README](../README.template.md) man kan ta utgangspunkt i.

I README må det også fremkomme et kontaktpunkt for koden/teamet. Dersom repoet er åpent _skal_ det fremkomme en måte omverden kan ta kontakt på (e-post, navn på person, osv).

## Codeowners

Her må teamet stå som eiere, på formatet: `* @helse-sorost/navn-på-team`. Eget team opprettes da på GitHub via helse-sorost-organisasjonen. Enkeltpersoner skal ikke stå som codeowners.

Liste over tilgjengelige HSØ-team på Github er her:
https://github.com/orgs/helse-sorost/teams

Det maskinlesbare navnet på teamet er det man ser i URL-en når man går inn på teamet sin Github-side.

Eksempel `CODEOWNERS`-fil:

```
* @helse-sorost/navn-på-team
```

# Contributing

Her kan vi oppgi hvordan andre både eksterne og ev. interne kan bidra på kodebasen, ev. spesifisere at kodebasen ikke tar imot bidrag.

> Hvis kodebasen åpner for bidrag, sjekk at dere også følger retningslinjene i [Åpne for bidrag](åpne-for-bidrag.md).

Eksempel `CONTRIBUTING`-fil:

```markdown
Dette prosjektet er åpent for å akseptere funksjonsforespørsler og bidrag fra åpen kildekode-fellesskapet.
Vennligst fork repoen og start en ny branch å jobbe med.

## Bygge lokalt

Dette prosjektet bruker [Gradle](https://gradle.org/) som byggeverktøy.
En Gradle Wrapper er inkludert i koden, så du trenger ikke å administrere din egen installasjon.
For å kjøre et bygg, utfør følgende kommado:
./gradlew clean build

Dette vil kjøre alle trinnene som er definert i `build.gradle.kts` filen.

## Testing

Hvis du legger til en ny funksjon eller feilretting, sørg for at det er riktig testdekning.

## Pull Request tilbakemelding

Hvis du har en branch på forken din som er klar til å slås sammen, vennligst opprett en ny pull-request. Vedlikeholderne vil gå gjennom for å sikre at retningslinjene ovenfor er fulgt, og hvis endringene er nyttige for alle bibliotekbrukere, vil de bli slått sammen.
```

## Sanering av gammel kode

Om det er flytting av eksisterende kode må både [kode og Git historikk vaskes](sikkerhetsvask.md).

## Scanning etter kjente sårbarheter i biblioteker

Programbiblioteker man er avhengig av må være uten kjente [sikkerhetshull](sårbarhetsscan.md).

## Commit-meldinger

Git historikken bør ha så mye verdi som mulig. Vi har derfor en [anbefaling til gode commit meldinger](commit-meldinger.md).
