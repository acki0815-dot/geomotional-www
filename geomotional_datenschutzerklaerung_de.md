# Datenschutzerklärung für die App „Geomotional“ (Android)

**Stand:** 2025-08-27 • **Version:** 1.0  
**Diensteanbieter / Verantwortlicher i.S.d. DSGVO:**  
**Sven Ackermann** (Privatperson)  
**Anschrift:** An den Ladillen 31, 27798 Hude, Germany  
**E-Mail (Support):** support@geomotional.app

---

## 1. Geltungsbereich
Diese Datenschutzerklärung gilt für die Android-App **„Geomotional“**. Sie erläutert Art, Umfang und Zwecke der Verarbeitung personenbezogener Daten innerhalb der App sowie der verbundenen Backend-Dienste.

## 2. Kurzüberblick (Was passiert mit deinen Daten?)
- **Kernfunktionen:** Spots auf Karte erstellen, Medien an Spot anhängen (nur Ersteller), „Vor-Ort-Entsperrung“ (Radius ca. 50 m), Teilen mit anderen, Nähe-Hinweise (Push), Navigation zum Spot.
- **Offline-First:** Daten werden lokal (verschlüsselt) zwischengespeichert und bei Verbindung synchronisiert.
- **Account:** Gastmodus möglich; optional Account per **Magic-Link** (E-Mail) und **Google-Login**. (Apple-Login später)
- **Kinder/Mixed-Audience:** App kann von Kindern genutzt werden. Beim ersten Start fragen wir das **Geburtsjahr** ab. Für unter 13 Jahren aktivieren wir einen **Kindermodus** mit eingeschränkter Datenerhebung.
- **Keine Werbung in V1:** In der MVP-Version werden **keine Anzeigen** ausgeliefert.
- **Sicherheit:** Verschlüsselung am Gerät (AES-GCM; Key im Android Keystore), Transport nur per HTTPS/TLS.

## 3. Kategorien personenbezogener Daten
### 3.1 Kontodaten & Identität
- **Anzeige-Name** (Pflicht), **Avatar** (optional)
- **E-Mail** (für Magic-Link) bzw. Google-Konto-ID-Token (bei Google-Login)

**Zweck:** Kontoerstellung, Anmeldung, Synchronisation, Teilen/Einladungen.  
**Rechtsgrundlage:** Art. 6 Abs. 1 lit. b DSGVO (Vertragserfüllung), ggf. lit. a (Einwilligung).

### 3.2 Standortdaten
- **Präzise Standortdaten** zur Erstellung/Entsperrung von Spots, **Geofencing** (Hintergrund-Standort, falls zugelassen).
- Speicherung der **Spot-Koordinate**; **kein permanentes Bewegungsprofil**.
- Bei Kindermodus beschränken wir die Verarbeitung auf das für die Funktion notwendige Maß.

**Zweck:** Kernfunktion „Vor-Ort-Entsperrung“, Nähe-Hinweise, Navigation.  
**Rechtsgrundlage:** Art. 6 Abs. 1 lit. b DSGVO; für Hintergrund-Standort **Einwilligung** (Art. 6 Abs. 1 lit. a).

### 3.3 Medien & Inhalte
- **Vom Spot-Ersteller** hochgeladene **Fotos/Videos/Audio/Text** (Eingeladene: in V1 nur **Kommentare/Reaktionen**, keine Medien).
- Optional: **Thumbnails/komprimierte Previews** am Gerät und im Storage.

**Zweck:** Bereitstellung von Spot-Inhalten, Teilen, Offline-Nutzung.  
**Rechtsgrundlage:** Art. 6 Abs. 1 lit. b DSGVO.

### 3.4 Kommunikations- und Nutzungsdaten
- **Push-Tokens** (Firebase Cloud Messaging – FCM)
- **Technische Ereignisse/Crash-Daten** (Firebase Crashlytics), **Nutzungsmetriken** (Firebase Analytics – im Kindermodus reduziert bzw. deaktiviert)
- **Einladungen/Sharing-Metadaten** (wer darf was sehen).

**Zweck:** Benachrichtigungen, Stabilität, Qualitätssicherung, Missbrauchsprävention.  
**Rechtsgrundlage:** Art. 6 Abs. 1 lit. f DSGVO (berechtigtes Interesse: App-Betrieb, Sicherheit); ggf. lit. a (Einwilligung für Benachrichtigungen).

## 4. Berechtigungen (Android)
- **Standort**: „Während der Nutzung“ für Karte/Nähe, **„Immer erlauben“** (optional) für Geofencing im Hintergrund.
- **Benachrichtigungen**: für Nähe-Hinweise, Einladungen, Besuchs-/Feedback-Infos.
- **Kamera/Mikrofon/Dateien**: nur wenn du Medien an Spots anfügst.
- **Netzwerkzugriff**: Synchronisation, Karten, Einladungen.

Du kannst Berechtigungen in den System-Einstellungen jederzeit widerrufen; einzelne Funktionen sind dann ggf. nicht nutzbar.

## 5. Verarbeitung im Detail
### 5.1 Offline-Speicherung
- **SQLite/Room** für Metadaten (Spots, Freigaben, Kommentare).  
- **Lokaler App-Speicher** für Thumbnails/Previews; **Verschlüsselung at rest** (AES-GCM, Schlüssel im Android Keystore).
- **LRU-Cache**; Nutzer kann Inhalte „**Offline speichern**“ (pinnen).

### 5.2 Cloud-Dienste (Auftragsverarbeiter)
- **Supabase** (EU-Region, z. B. Frankfurt): Auth, Postgres-DB, Storage.  
- **Google Firebase**: **FCM** (Push), **Crashlytics** (Fehler), **Analytics** (Nutzung; im Kindermodus eingeschränkt/aus).
- **Google Maps SDK** (Kartenanzeige/Geocoding).

**Datenübermittlung in Drittländer:** Bei Google-Diensten kann eine Übermittlung in die USA stattfinden. Wir stützen dies auf **EU-Standardvertragsklauseln (SCCs)**; zudem aktivieren wir, wo verfügbar, EU-Regionseinstellungen. Supabase betreiben wir in der **EU-Region**.

## 6. Zwecke & Rechtsgrundlagen im Überblick
- **Bereitstellung der App-Funktionen (Vertrag)**: Art. 6 Abs. 1 lit. b DSGVO  
- **Einwilligungspflichtige Funktionen** (z. B. Hintergrund-Standort, Benachrichtigungen): Art. 6 Abs. 1 lit. a DSGVO  
- **Sicherheit, Missbrauchsprävention, Qualität**: Art. 6 Abs. 1 lit. f DSGVO  
- **Gesetzliche Pflichten** (z. B. Aufbewahrungspflichten): Art. 6 Abs. 1 lit. c DSGVO

## 7. Kinder & Jugendliche (Mixed-Audience)
- **Altersabfrage (Geburtsjahr)** beim ersten Start.  
- **Unter 13 Jahren**: **Kindermodus** (keine personalisierte Werbung, eingeschränkte Analytics, reduzierte Datenverarbeitung).  
- **Unter 16 Jahren**: Für Funktionen, die eine **Einwilligung** erfordern, holen wir – soweit erforderlich – die **Zustimmung der Sorgeberechtigten** ein oder schränken die Funktion ein.  
- Wir sammeln **nicht wissentlich** zusätzliche Daten von Kindern über das erforderliche Maß hinaus.

## 8. Teilen/Empfänger
- Andere Nutzer, denen du **explizit Zugriff** gewährst (Einladungslink oder Nutzername).  
- **Auftragsverarbeiter**: Supabase, Google Firebase / Google Maps (s. oben).  
- **Keine** Weitergabe an sonstige Dritte zu Werbezwecken.

## 9. Speicherdauer & Löschung
- **Accountdaten/Spots/Kommentare**: bis zur **Löschung durch dich** oder Beendigung deines Accounts.  
- **Uploads/Medien**: bis zur Löschung durch dich; ggf. Lifecycle-Regeln (Archivierung/Löschung nicht gepinnter Originale nach X Tagen).  
- **Crash-/Analysedaten**: gemäß Vorgaben der jeweiligen Dienste, typischerweise wenige Monate.  
- **Lokaler Cache**: automatisch nach Speicher-/Nutzungsregeln; manuell entfernbar.

## 10. Deine Rechte (DSGVO)
- **Auskunft**, **Berichtigung**, **Löschung**, **Einschränkung**, **Datenübertragbarkeit**, **Widerspruch** gegen Verarbeitung auf Basis berechtigter Interessen.  
- **Widerruf** erteilter Einwilligungen mit Wirkung für die Zukunft.  
- **Beschwerde** bei einer Datenschutzaufsichtsbehörde, z. B. der für deinen Wohnsitz zuständigen.

Kontakt zur Ausübung deiner Rechte: support@geomotional.app

## 11. Sicherheit
- **Transportverschlüsselung (TLS)**, **Speicherverschlüsselung** am Gerät, **rollenbasierte Zugriffe** im Backend.  
- Regelmäßige Updates und **Least-Privilege-Prinzip** für Schlüssel/Token.

## 12. Automatisierte Entscheidungen/Profiling
- Es findet **keine** automatisierte Entscheidungsfindung im Sinne von Art. 22 DSGVO statt; kein Profiling.

## 13. Änderungen dieser Erklärung
Wir können diese Datenschutzerklärung anpassen, wenn Funktionen oder rechtliche Rahmenbedingungen sich ändern. Es gilt stets die in der App/auf der Website veröffentlichte aktuelle Version.

---

**Kontakt:**  
Sven Ackermann
An den Ladillen 31
27798 Hude
Germany
