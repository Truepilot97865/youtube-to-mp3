Archive ZIP : youtube-to-mp3-release-v1.zip
Script d’installation automatique : scripts/oneclick_installer.ps1
SHA256 du ZIP (v1.0) :
2EC8AD2D33D18BF79EAF17D4173B04FE9C7D263911A7226450802ECECF13D81F
Installation (procédure recommandée, sécurisée)

Télécharger et vérifier le script d’installation (inspecter le contenu) :
Invoke-WebRequest -UseBasicParsing -OutFile oneclick_installer.ps1 
Ouvrez ensuite le script pour vérification : notepad oneclick_installer.ps1

(Optionnel mais recommandé) Vérifier l’intégrité du ZIP après l’avoir téléchargé depuis la Release :
Get-FileHash -Algorithm SHA256 .\youtube-to-mp3-release-v1.zip
La valeur attendue :
2EC8AD2D33D18BF79EAF17D4173B04FE9C7D263911A7226450802ECECF13D81F

Lancer l’installation (après vérification) — le script demandera l’élévation UAC :
powershell -ExecutionPolicy Bypass -File .\oneclick_installer.ps1 -ProjectZipUrl 

Que fait le script

Demande l’élévation (UAC) — l’utilisateur doit accepter.
Installe Python automatiquement (si absent) et ajoute Python au PATH.
Télécharge et installe FFmpeg, définit FFMPEG_LOCATION.
Crée un environnement virtuel, installe les dépendances du projet.
(Optionnel) construit l’exécutable Windows et lance l’application GUI.
Utilisation après installation

Ouvrir l’application GUI → coller l’URL YouTube → cliquer « Télécharger et convertir ».
Les MP3 sont enregistrés par défaut dans : %USERPROFILE%\Downloads\YouTubeToMP3 (le dossier s’ouvre automatiquement à la fin).
Sécurité & recommandations

N’exécutez pas ce script sans l’avoir inspecté si vous ne faites pas confiance à la source.
Vérifiez la SHA256 du ZIP avant exécution.
L’UAC est normale : elle est requise pour installer Python/FFmpeg et écrire dans Program Files.
Support & dépannage


Réalisée par un jeune de 16 ans, si besoin d'aide veuillez me contactez
Si l’installation échoue ou si l’exécutable ne fonctionne pas contactez moi en MP si néccessaire

Pour assistance immédiate, copiez/collez la sortie d’erreur dans l’issue.
