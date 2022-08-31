# Új repo létrehozása

-C:\Program Files\Git\etc\gitconfig" fájl szerkesztése azért, hogy NE tárolja el a Windows hitelesítés-kezelőjében a github-os jelszót:
 [credential]
	helper = manager-core // HELYETT (üresen kell hagyni): helper =
 Ekkor NEM ugrik fel a hitelesítő ablak (hanem parancssorban be fogja kéri a tokent),
 és NEM tárolja el a Windows hitelesítés-kezelőjében!
- a gihub oldalon létrehozni az új repót
- a saját gépre klónozni az üres repot: git clone <url>
- a config fájlba belejavítani (az url-be beszúrni a token@ szót a github.com elé)
- a helyi repoba menteni a módosításokat( >git add . majd >git commit -m "first")
- push-al feltenni a távoli repóba (fogja kérni a saját személyes tokent)