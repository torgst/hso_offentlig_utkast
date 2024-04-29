# Åpne for bidrag i kodebasen

Det er viktig at kodebaser som åpner for bidrag fra andre blir aktivt fulgt opp. Dette er for å sikre at bidragsytere får en god opplevelse, og at kodebasen forblir sunn og vedlikeholdbar.
Det er også viktig at kodebaser som åpner for bidrag er sikret slik at uvedkommende ikke kan legge inn skadelig kode.

## Hovedregelen er fork-baserte bidrag

> Hovedregelen for bidrag til kodebaser er at bidragsytere skal lage en fork av kodebasen, gjøre endringer i denne, og så lage en pull request tilbake til hovedkoden.

Det er også mulig å legge til eksterne brukere som **outside collaborators**. Disse vil kunne jobbe i basen uten "SAML single sign-on" (altså uten å være en del av organisasjonen). Dette kan være aktuelt f.eks. hvis kodebasen skal deles med andre helseregioner.

> [!CAUTION]
> Brukere som legges til som **outside collaborators** vil ha også ha tilgang til "codespace secrets" hvis de oppretter codespaces i repo'et. Det er derfor viktig å bare gi slik tilgang etter en risikovurdering.

## Planlegge oppfølging

Sørg for at teamet har en plan for hvordan de følger opp innkommende bidrag. Det er viktig at det er minst én person i teamet som eier koden som er fast ansatt. Kodebaser som i sin helhet håndteres av innleide ressurser skal ikke åpnes for bidrag.

> TODO: avklare om vi er komfortable med en såpass enkel prosess, eller om det må beskrives nærmere?

## Sikre mot skadelig kode

> TODO: kan vi håndtere dette sentralt f.eks. via "rulesets"?

- all branch'er som deployer kode skal ha "protection rules" som krever:
  - Pull request
  - Code review og godkjenning fra CODEOWNERS før koden merges
  - Godkjenning av noen med skrivetilgang til repo for å trigge workflows
