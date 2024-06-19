# Retningslinjer for åpen IaC-kode

1. IaC-**moduler** som beskriver generelle komponenter og som baseres på `input` og `output` kan publiseres som åpen kildekode.
2. Utover det er hovedregelen er at IaC-kode _ikke_ skal inngå i repo som er `public`.\
   > Rasjonalet for dette er at det sjelden vil være _behov_ for å dele IaC-kode utenfor HSØ, samtidig som det er en risiko for at IaC-koden avslører mer om infrastrukturen vår enn vi ønsker.

## Åpne et repo som allerede inneholder IaC-kode

Kontakt CPO for en gjennomgang av IaC-koden for å avklare om den avslører sensitiv informasjon.

### Hvis IaC-koden avslører sensitiv informasjon

- Koden som skal åpnes må flyttes til et nytt repo **uten historikk** (kopier siste versjon av koden inn i et nytt repo).
- Det eksisterende repo'et benyttes for IaC-koden.

### Hvis IaC-koden ikke avslører sensitiv informasjon

- IaC-koden flyttes til et nytt repo (du kan f.eks. kopiere over hele repo'et, med historikk, og så slette alt som ikke er IaC).
- IaC-koden slettes fra eksisterende repo'et.
