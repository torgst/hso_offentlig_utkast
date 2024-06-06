# Retningslinjer for åpen kildekode i Helse Sør-Øst

> [!WARNING]
> Dette er et utkast til retnignslinjer for åpen kildekode i Helse Sør-Øst. Endelig versjon vil publiseres i Helse Sør-Østs offentlige organisasjon på Github.

## Introduksjon

Offentlig finansierte løsninger bør være offentlig tilgjengelig. Motivasjonen er da ikke hovedsakelig gjenbruk, selv om det selvsagt er en heldig bieffekt. Motivasjonen er først og fremst åpenhet og gjennomsiktighet i de digitale løsningene. Disse retningslinjene legger seg tett opptil retningslinjene fra tilsvarende retningslinjer fra [NAV](https://github.com/navikt/offentlig).

### Hvordan åpen kildekode skiller seg fra åpne standarder

Åpen kildekode er en måte å utvikle og distribuere programvare på. Koden skrives ofte i samarbeid, og den kan lastes ned, brukes og endres av hvem som helst. Se her for detaljer for MIT-lisensen som Helse Sør-Øst bruker https://tldrlegal.com/license/mit-license og https://en.wikipedia.org/wiki/MIT_License.
Åpne standarder er felles regler som lar enhver bruker lage kompatible og konsistente produkter, prosesser og tjenester. De er designet i samarbeid, er offentlig tilgjengelige og gratis eller til lave kostnader. Vær oppmerksom på at det likevel kan påløpe kostnader ved åpen kildekode. Migreringskostnader (til og fra) bør tas med i vurderingen.

### Hvordan åpne kildekode?

Du må lage en PR i admin-repoet og fylle ut sjekklisten som ligger i PR-malen. Følg fremgangsmåten beskrevet i [/helse-sorost/admin/RECIPES.md](https://github.com/helse-sorost/admin/blob/policy/RECIPES.md#gj%C3%B8re-ditt-repository-public).

## Åpen kildekode

### Ved å bruke åpen kildekode kan du:

- Nyttiggjøre deg allerede løste problemer med allmenn tilgjengelig teknologi
- Spare tid og ressurser på tilpassede løsninger for å løse sjeldne eller unike problemer
- Oppnå lavere implementerings- og driftskostnader

### Hvordan din kode kan bli bedre om den er åpen:

Å publisere koden og dataene dine fra begynnelsen av kodebasens levetid eller programmet ditt vil oppmuntre til:

- renere og godt strukturert kode som er enklere å vedlikeholde
- klarhet rundt data som må forbli beskyttet og hvordan det oppnås
- forslag til hvordan koden kan forbedres eller hvor sikkerheten kan forbedres

### Sikkerhet:

Åpen kildekode bidrar med alt fra transparens og hurtig respons på sikkerhetstrusler, til bedre tilpasset kode og støtte. Ved å utnytte den samarbeidende og transparente naturen til åpen kildekode kan organisasjoner bygge og vedlikeholde sikrere infrastrukturer. Dette vil til slutt bidra mot en mer robust sikkerhetsholdning (posture). HSØ gjør en rekke grep for å sikre koden før den publiseres ved blant annet hemmelighetscanning, IaC policy scanning og rutiner for publisering. Vi har stor tillit til koden vår og ønsker bidrag og tilbakemelding. Dette tror vi skjer best gjennom transparens og åpen kildekode.

### Ansvar:

> [!CAUTION]
> Teamet som eier koden har ansvaret for vurdere om koden er trygg å distribuere som åpen kildekode. Dersom koden overføres til et nytt team, må dette teamet gjøre en ny vurdering. Dette ansvaret gjelder i kodens levetid.

## Kvalitet og relevans:

All kode i Helse Sør-Øst skal holde [høy kvalitet](guider/kodekvalitet.md), uavhengig om den er åpen eller lukket. At en kodebase har lav kodekvalitet er ikke i seg selv et argument for å la være å åpne den for innsyn, men et argument for å arbeide med å forbedre kodekvaliteten.

## Krav til åpne repo under github.com/helse-sorost

> [!IMPORTANT]
> Alle repositories på Github knyttet til Helse Sør-Øst skal, uavhengig av synlighet, oppfylle kravene under.

_Dersom repositoryet ditt oppfyller disse kravene, så er det opp til teamet selv om de ønsker å ha koden åpent eller lukket._

### Lisens:

Alle repoer må ha en egen LICENSE-fil (plain text) eller en LICENSE.md-fil (markdown). Se [lisensiering.md](LISENSIERING.md) for detaljer om hvilke lisenser vi bruker i Helse Sør-Øst.

### README.md:

Alle repoer må ha en forklarende Read Me, enten som plaintext (README) eller som markdown (README.md). Vi oppfordrer teams til å beskrive hensikten med repoet, hvordan man bygger/tester koden samt hvordan man kan komme i kontakt med teamet på (både som intern og ekstern bruker). Bruk [denne templaten](README.template.md).

### Eierskap:

GitHub har støtte for en spesiell fil som heter CODEOWNERS som angir hvilke team som eier koden, eller deler av den. Formatet i filen ligner mye på .gitignore, men følgende eksempel er et greit utgangspunkt for de fleste:

```
* @helse-sorost/navn-på-team
```

Dette betyr at teamet _navn-på-team_ eier hele kodebasen (\* er wildcard). Vi ønsker ikke at enkeltpersoner skal stå oppført her.

### Sikkerhetsvask

Både git-historikk og kode må vaskes for eventuelle hemmeligheter og personsensitive opplysninger. Her finnes det mange ulike verktøy man kan benytte seg av, og det finnes en liten [guide på GitHub](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository) om dette.

### Risikovurdering

> TODO: Se om vi kan få en guide på dette.

Før koden publiseres må teamet gjøre en risikovurdering. ~~Team Tryggnok har lagd et verktøy for å gjennomføre en slik ROS-analyse. Ta kontakt med teamet på Slack i kanalen #tryggnok.~~

## Kode som ikke kan åpnes

Vi må holde noe data og kode lukket:

- nøkler og legitimasjon

> [!NOTE]
> Kodebaser som vurderes til å ikke kunne være åpne skal ha et avsnitt i README hvor beslutningen begrunnes så konkret som mulig.
> Eks på begrunnelser om hvorfor kodebasen er lukket: ~~[aad-iac](https://github.com/navikt/aad-iac) og [loginservice](https://github.com/navikt/loginservice)~~

> TODO: Finne tilsvarende eksempler fra Helse Sør-Øst (må vel lages først...)

### Nøkler og legitimasjon

Du må holde hemmelige data som nøkler eller legitimasjon lukket, fordi denne informasjonen kan tillate noen å få tilgang til systemet ditt. Du må videre holde kode som bruker hemmeligheter borte fra hemmelighetene i seg selv. Dette inkluderer lagring av hemmelige nøkler og legitimasjon. Du kan deretter åpne koden mens du holder hemmelighetene lukket og sikker. Du skal bruke et separat system for å lagre og sikre hemmelighetene dine, men la applikasjoner bruke dem der det er nødvendig. Et slikt system sørger for at bare autoriserte ansatte får tilgang til nøklene. Systemet gjør det også lettere å tilby forskjellige nøkler for forskjellige miljøer og rotere nøkler om nødvendig.

> Følg veiledningen for å håndtere sikkerhetsproblemer hvis du ved et uhell eksponerer en hemmelighet. (TODO)

## Publisere bibliotek

Hvis du lager et bibliotek som er naturlig å publisere på f.eks. Nuget, NPM eller PyPI så kan du gjøre det med Github Actions.

> TODO: vurdere om pakker som publiseres på pypi.org, dockerhub, powershell gallery eller lignende burde gjøres med en offisiell Helse Sør-Øst konto, og ev. etablere en rutine for opprettelse av offisielle kontoer på slike steder.
> TODO: vurdere å lage noen reusable github workflows som er satt opp for publisering mot disse tjenestene.
> TODO: vurdere signering av pakker med offisielt HSO sertifikat (enten som et krav, eller at vi opplyser om hvor man kan få tilgang til codesign sertifikat).

## Er du klar?

Sjekk ut guiden om [nye repo](guider/nye-repo.md). Husk at det er teamet selv som tar det ansvarlige valget om koden kan åpnes eller ikke.
