# velpTEC Weiterbildung -- Modul: GitHub/GitLab -- Teilprüfung 1

***bearbeitet von: Susanne Nienhaus***, ***bearbeitet am: 21.03.25***

## Aufgabe a: GitHub Repository Setup
1. bei GitHub anmelden: 

    - auf github.com melde ich mich mit meinem Benutzerkonto an

    ![GitHub-Seite nach der Anmeldung](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeA1_AnmeldenBeiGitHub.jpg?raw=true)


2. ein neues Repository erstellen:
    
    - ich klicke oben rechts auf der Seite auf "+ New"
    - es öffnet sich ein Formular, mit dem ich ein neues Repository erstellen kann
    - ich gebe den Namen "MeinProjekt" an und füge eine kurze Beschreibung hinzu
    - ich wähle aus, dass das Projekt erstmal privat ist und dass eine README-Datei automatisch hinzugefügt werden soll 

    ![ausgefülltes Formular, um das Repo zu erstellen](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeA2_NeuesRepositoryErstellen.png?raw=true)

    - ich klicke unten rechts auf "Create repository"


3. URL notieren: 

    - um die URL des neuen Repositorys zu notieren, klicke ich auf der Projektseite auf "<> Code"
    - im DropDown sehe ich die URL: https://github.com/s-n-hub/MeinProjekt.git

    ![URL des neuen Repos anzeigen lassen](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeA3_UrlNotieren.png?raw=true)



## Aufgabe b: SSH-Schlüssel erstellen
4. Terminal öffnen:

    - ich öffne GitBash (Windows)

    ![Geöffnetes leeres Terminal](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeB4_Terminal%C3%96ffnen.png?raw=true)


5. prüfen, ob ich einen Schlüssel habe:

    - ich gebe ins Terminal ein: ls ~/.ssh/
    - die Ausgabe zeigt mir meinen SSH-Schlüssel an

    ![Eingabe und Ausgabe im Terminal](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeB5_SSH_Checken.png?raw=true)

    - ich kann sehen, dass ein SSH-Schlüssel bereits eingerichtet ist
    - ich aktiviere den SSH-Agent, in dem ich im Terminal "eval "$(ssh-agent -s)" eingebe und dann "ssh-add ~/.ssh/id_rsa"
    - ich gebe mein Passwort für den Schlüssel ein

    ![Befehle zum Aktivieren des SSH-Agents](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeB5_SSH_Agent.png?raw=true)

    - die Schritte 6 und 7 kann ich überspringen



## Aufgabe c: Lokales Repository einrichten und Workflow
8. im Terminal zum Verzeichnis navigieren:

    - um in das Verzeichnis zu navigieren, in dem ich mein lokales Repository haben möchte, navigiere ich mit einigen cd-Befehlen im Terminal

    ![Navigation mit cd im Terminal](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC8_insVerzeichnisNavigieren.png?raw=true)


9. GitHub-Repository 'MeinProjekt' klonen:

    - um das GitHub-Repository in meiner lokalen Umgebung verfügbar zu machen, klone ich es, indem ich in der GitBash folgenden Befehl eingebe: git clone git@github.com:s-h-hub/MeinProjekt.git
    - an der Ausgabe im Terminal erkenne ich, dass das Klonen erfolgreich war

    ![Klonen des Repos im Terminal](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC9_RepoKlonen.png?raw=true)


10. in das Verzeichnis navigieren:

    - um in das Projektverzeichnis zu wechseln, gebe ich im Terminal "cd MeinProjekt" ein

    ![Navigieren mit cd im Terminal](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC10_insVerzeichnisNavigieren.png?raw=true)


11. Git konfiguireren: 

    - ich konfiguriere in Git meinen Usernamen, in dem ich im Terminal eingebe: git config user.name "Susanne Nienhaus"
    - ich konfiguriere meine E-Mail-Adresse, indem ich im Terminal eingebe: git config user.email "susanne@nienhaus.ws"

    ![Konfigurationsbefehle im Terminal](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC11_GitKonfigurieren.png?raw=true)


12. Neue Datei main.py hinzufügen: 

    - ich erstelle die Datei main.py im Terminal mit dem Befehl "touch main.py"
    - ich stage die neue Datei mit dem Befehl: git add main.py"
    - ich erstelle einen Commit mit dem Befehl: git commit -m "Initialer Commit"
    - an der Ausgabe im Terminal sehe ich, dass der Commit erfolgreich war - die neue Datei ist nun im lokalen Repository gespeichert

    ![Datei hinzufügen im Terminal](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC12_neueDateiHinzuf%C3%BCgen.png?raw=true)


13. Neuen Branch 'feature' erstellen: 

    - um einen neuen Branch namens 'feature' zu erstellen, gebe ich im Terminal ein: git checkout -b feature
    - mit diesem Befehl wechsele ich automatisch auf diesen Branch, wie auch die Ausgabe zeigt

    ![Branch erstellen und switchen im Terminal](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC13_neuerBranchFeature.png?raw=true)


14. weitere Datei "utils/database.py" hinzufügen

    - mit dem Befehl mkdir erstelle ich im Terminal zunächst das Verzeichnis 'utils'
    - die Datei erstelle ich mit dem Befehl 'touch utils/database.py'

    ![neue Datei erstellen im Terminal](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC14_neueDateiErstellen.png?raw=true)

    - um die erstellte Datei in den Staging-Bereich des Feature-Branches hinzuzufügen, gebe ich den Befehl 'git add utils/database.py' im Terminal ein
    - ich erstelle dann einen einen neuen Commit mit dem Befehl: git commit -m "Neue Funktion hinzugefügt"

    ![neue Datei committen im Terminal](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC14_neueDateiHinzugef%C3%BCgt.png?raw=true)


15. die Datei main.py bearbeiten und die Änderung committen:

    - ich öffne die Datei in VSCode und bearbeite dort die erste Zeile, indem ich einen Kommentar verfasse

    ![Datei in VSCode bearbeiten](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC15_DateiBearbeiten.png?raw=true)
    
    - der Befehl 'git status' im Terminal zeigt an, dass die Änderung der Datei von Git zur Kenntnis genommen wurde  
    - um die Änderung zu stagen, nutze ich im Terminal dann den Befehl: git add main.py
    - ich füge den aktuellen Stand der Datei durch einen Commit ins Repository hinzu mit dem Befehl: git commit -m "Hauptdatei aktualisiert"
    
    ![Datei im Terminal committen](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC15_%C3%84nderungCommitten.png?raw=true)


16. zum main-Branch zurückwechseln:

    - ich wechsele den Branch von 'Feature' zu 'Main', indem ich 'git checkout main' im Terminal eingebe
    
    ![Branch wechseln im Terminal](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC16_BranchWechseln.png?raw=true)


17. main.py bearbeiten auf main-Branch committen

    - auch hier öffne ich die Datei main.py in VSCode und ändere die erste Zeile durch einen Kommentar (der sich vom Kommentar unterscheidet, den ich im Feature-Branch hinzugefügt hatte)

    ![Datei bearbeiten in VSCode](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC17_DateiBearbeiten.png?raw=true)

    - der 'git status'-Befehl im Terminal bestätigt, dass die Änderung erkannt wurde
    - mit 'git add main.py' überführe ich die aktuelle Version in den Staging-Bereich
    - ich erstelle einen Commit mit der Änderung durch den Befehl: git commit -m "Hauptdatei aktualisiert"   
    
    ![Datei im Terminal committen](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC17_%C3%84nderungCommitten.png?raw=true)


18. die Branches mergen:

    - um die Branches zu mergen, nutze ich im Terminal den Befehl 'git merge feature'
    - die Ausgabe klärt darüber auf, dass in der Datei main.py ein Merge-Konflikt vorliegt, so dass kein automatischer Merge durchgeführt werden kann

    ![Merge-Versuch im Terminal](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC18_MergeVersuch.png?raw=true)

    - ich öffne die Datei main.py in VSCode
    - dort werden mir die beiden konfligierenden Zeilen übersichtlich angezeigt
    
    ![Merge-Konflikt in VSCode](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC18_MergeKonflikt.png?raw=true)

    - ich entscheide mich für eine der von VSCode vorgeschlagenen Lösungen und akzeptiere beide Änderungen, so dass die Kommentare nun zwei Zeilen untereinander stehen
    
    ![Lösung des Konflikts in VSCode](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC18_MergeKonfliktL%C3%B6sung.png?raw=true)

    - nachdem ich die Änderung gespeichert und VSCode geschlossen habe, schiebe ich die Datei mit 'git add main.py' abermals in den Staging-Bereich
    - 'git status' zeigt u.a. an, dass der Konflikt behoben ist, aber der Merge noch nicht abeschlossen wurde
    - ich nutze 'git commit', um die Änderung ins Repository zu schieben
    - es öffnet sich im Editor ein Vorschlag für die Commit-Message für den Merge
    - indem ich das Fenster schließe, akzeptiere ich sie

    ![Commit-Message in VSCode](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC18_Commit_Message.png?raw=true)
    
    - der Merge wird nun durchgeführt und abgeschlossen

    ![Merge abschließen im Terminal](https://github.com/s-n-hub/MeinProjekt/blob/main/Screenshots-TP/AufgabeC18_MergeAbschlie%C3%9Fen.png?raw=true)
    
