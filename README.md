# Installation av Docker Desktop
Eftersom många (inkl jag själv) fick problem med installationen av virtualiseringsmiljön Docker, applikationen Docker Desktop, kommer här en lite guide. Googlar man lite på "Docker desktop starting" så verkar det finnas fler som upplevt strul. *Guiden här gäller för Windows*.

Om du har en installation som inte fungerar så börja med att avinstaller Docker Desktop innan stegen nedan.

---

## Installera Docker Desktop i Windows

Docker Desktop använder WSL *Windows Subsystem for Linux*.  Det är en funktion i Windows som tillåter utvecklare att köra en Linux-miljö utan behov av en separat virtuell maskin eller dubbel uppstart.

För att använda version 2 av WSL krävs Windows 10 version 1903 eller senare (Build 18362).


## Steg 1: Windows funktioner 
Kontrollera att datorn kan hantera Hyper-V genom att visa installerade funktioner i Windows.

Gå via kontrollpanelen eller skriv `optionalfeatures` i Windows sökfält.

Se till att följande funktioner är aktiverade

- Hyper-V (och underliggande Hanteringsverktyg och plattform)
- Windows-undersystem för Linux

**Starta om datorn**

## Steg 2: Uppdatera Linux kernel

Starta en webbläsare och ladda ner senaste installtionsfilen för WSL, installera därefter uppdateringen

`https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi`

## Steg 3: Ange version för Windows-undersystem för Linux

Starta PowerShell, och kör följande kommando:

`wsl --set-default-version 2`

## Steg 4: Installera Docker Desktop

Hämta installationsfilen för Docker Desktop. Den förvalda bör fungera, men det går annars att hitta olika versioner via webbplatsen, ex en tidigare version som jag testat med framgång.

`https://docs.docker.com/desktop/release-notes/#4120`

När installationsfilen är hämtad, visa filen i utforskaren. Högerklicka därefter på filen och installera genom att välja *Kör som administratör*.

**Starta om datorn**

När du efter omstart därefter startar Docker Desktop kommer du först få acceptera villkoren. Därefter kommer förhoppningsvisa applikationen starta - för mig har det tagit allt från 10 sek till en dryg minut.

