# Új repo létrehozás

- a Github fiókban létre kell hozni egy Personal Access Token-t (PAT : Settings>Developer Settings)
- ajánlatos a tokent egy privát repóba elmenteni, mert az ablak bezárása után többet nem lehet megnézni(csak újat lehet létrehozni, meg törölni)
- azért, hogy NE tárolja el a Windows a hitelesítés-kezelőjében a github-os jelszavunkat, meg kell nyitni szerkesztésre a git config fájlt az alábbi paranccsal:

git config --system -e

Majd a helper attribútum értékét üresen kell hagyni

Ezek után NEM ugrik fel a hitelesítő ablak (hanem parancssorban be fogja kéri a tokent), NEM tárolódik el a Windows hitelesítés-kezelőjében (Credential Manager-ben)!

Egy másik megoldás:

git config --system --unset credential.helper

(Rendszergazdai jog szükségeltetik!)

- a github oldalon egy új üres repó létrehozása
- a saját gépre klónozni az üres repot: git clone <url>
- a config fájlba belejavítani (az url-be beszúrni a token@ szót a github.com elé)
- a helyi repoba menteni a módosításokat( >git add . majd >git commit -m "first")
- push-al feltenni a távoli repóba (fogja kérni a saját személyes tokent)