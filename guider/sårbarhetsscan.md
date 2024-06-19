# Scanneverktøy

Det oppdages jevnlig sikkerhetshull i tredjeparts rammeverk og biblioteker.
For å minske sannsynligheten for at vår kode også blir sårbar som følge av dette har Helse Sør-Øst kjøpt tilgang til [GitHub Advanced Security](https://docs.github.com/en/get-started/learning-about-github/about-github-advanced-security) som inneholder flere verktøy for å beskytte koden.

Verktøyene under er aktivert for alle repoer i vår enterprise konto. Et grunnleggende sikkerhetsnivå vil alltid være aktivert, men administratorer for hvert enkelt repo kan finjustere noen av innstillingene (se detaljer under [Oppskrifter](https://github.com/helse-sorost/admin/blob/main/RECIPES.md)).

| Verktøy           | Formål/beskrivelse                                                                                                              |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Dependabot        | Sjekker avhengigheter for kjente sårbarheter og varsler deg jevnlig hvis det dukker opp nye sårbarheter.                        |
| CodeQL analyse    | Verktøy for SAST (Static Application Security Testing), dvs. at det scanner koden for potensielle sikkerhetshull.               |
| Secret scanning   | Varsler hvis hemmeligheter er lagt inn i koden.                                                                                 |
| Dependency review | Gir oversikt over endringer i avhengigheter når du oppretter en PR. Sjekker også at alle avhengigheter har kompatible lisenser. |

> TODO: vurdere om vi skal ha _ytterligere_ verktøy enn Github Advanced Security.
