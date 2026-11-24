# Sikkerhet

Dette gjelder alle repoer i organisasjonen som ikke har sin egen `SECURITY.md`.

## Rapportere et sikkerhetsproblem

Ikke opprett en offentlig issue. Bruk **Report a vulnerability** under fanen **Security** i repoet, så bare
vedlikeholderne ser rapporten. Beskriv hva du fant, hvordan det kan gjenskapes, og hva det påvirker. Vi svarer så
fort vi kan.

Rapporten kan skrives på norsk eller engelsk.

## Hvis en push stoppes på grunn av en hemmelighet

Push protection stoppet pushen fordi en commit inneholder noe som ligner en hemmelighet.

1. Ikke omgå blokkeringen, med mindre verdien er en testverdi eller et falskt treff.
2. Fjern hemmeligheten fra commiten. Er den i den siste commiten, retter du filen og kjører `git commit --amend`. Er
   den lenger bak, bruker du `git rebase -i` og retter den commiten.
3. Har hemmeligheten vært pushet eller delt noe sted, regnes den som lekket: trekk den tilbake og lag en ny.
4. Legg den nye hemmeligheten i et GitHub-miljø som bare tillater `main`, aldri i koden.
