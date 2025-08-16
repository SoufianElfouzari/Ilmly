# Ilmly

## Projektübersicht
Tullab Al-Ilm ist eine Lernsoftware, die es Benutzern ermöglicht, Notizen zu erstellen, zu verwalten und mit der Community zu teilen. Zusätzlich integriert die Software religiöse Inhalte wie Hadithe und Ayat, bietet Community-Funktionen und ein Marketing-Webprojekt zur Nutzergewinnung.

---

## User Stories

- **Als Benutzer** möchte ich Notizen in verschiedenen Formaten erstellen und organisieren, damit ich effizient lernen kann.  
- **Als Benutzer** möchte ich direkten Zugriff auf Hadith- und Ayat-Texte haben, um das Lernen mit authentischen Quellen zu verbinden.  
- **Als Administrator** möchte ich Community-Aktivitäten überwachen und moderieren, um eine sichere und produktive Umgebung zu gewährleisten.  
- **Als Marketing-Team** möchte ich eine ansprechende Homepage und SEO-optimierte Inhalte haben, um neue Benutzer anzuziehen.  

---

## Anforderungen

### Lernsoftware & Community
- Rich Text Notizen erstellen, speichern und bearbeiten.
- Notizen teilen, sortieren und kategorisieren.
- Community-Feed, Gruppen und Chat zur Förderung von Interaktion.
- Benachrichtigungen & Einstellungen für individuelle Anpassungen.
- Export-Funktion für Notizen in PDF oder andere Formate.
- Hadith & Ayat Such- und Einfügefunktion.

### Marketing-Webprojekt
- Responsive Homepage mit Formularhandling.
- SEO-optimierte Inhalte.
- Authentifizierung und Autorisierung für Marketing-Formulare.
- Echtzeit-Funktionen per WebSocket für interaktive Elemente.

---

## Functional Requirements (Alpha Version) – Ilmly

---

### 1. User Authentication
❌ Login-Screen implementieren (Desktop)  
❌ Login-Screen implementieren (Tablet)  
❌ Login-Screen implementieren (Mobile)  
❌ Appwrite als Auth-Backend nutzen  
❌ Session-Management vorbereiten (Auto-Login, Token-Validierung)  
❌ Fehlerbehandlung für falsche Credentials anzeigen  
❌ Routing implementieren  
❌ Passwort vergessen Screen (Desktop, Tablet, Mobile)  
❌ Passwort vergessen Screen UI verbessern (Low)  

---

### 2. Dashboard / Navigation
❌ Grundlayout: Sidebar + Hauptbereich  
❌ Platzhalter für zukünftige Module (Notizen, Community, Statistik)  
❌ Responsives Layout für Small / Medium / Large Screens (High)  

---

### 3. Notiz-Management
❌ Notizenübersicht anzeigen  
❌ Notizen erstellen  
❌ Notizen bearbeiten  
❌ Notizen löschen  
❌ Rich Text Editor implementieren (bold, italic, underline, listen, links)  
❌ Bilder und Medien in Notizen einfügen  
❌ Notizen sortieren und filtern (Datum, Kategorie, Favoriten)  
❌ Multi-Step Form für komplexe Notizen vorbereiten  
❌ Notizen exportieren (PDF, ggf. andere Formate)  
❌ Offline-Verfügbarkeit der Notizen vorbereiten  
❌ Responsives Layout (Small / Medium / Large)  

---

### 4. Hadith & Ayat Integration
❌ Suche nach Hadithen implementieren  
❌ Suche nach Ayat implementieren  
❌ Texte in Notizen einfügen  
❌ Favoriten / Lesezeichen-System  
❌ Offline-Zugriff vorbereiten  
❌ Filter nach Sammlung, Quelle, Thema  

---

### 5. Community / Chat
❌ Community Feed anzeigen  
❌ Gruppen erstellen, beitreten und verwalten  
❌ Chat-System implementieren (1:1 und Gruppen)  
❌ Benachrichtigungen für neue Posts, Kommentare, Nachrichten  
❌ Moderationstools für Admins vorbereiten  
❌ Benutzerprofil & Einstellungen implementieren  

---

### 6. PDF-Integration / Export
❌ GET-Request an lokale oder Cloud-API vorbereiten  
❌ Query-Parameter für Header, Footer, Notizen, Bilder implementieren  
❌ PDF-Download vorbereiten  
❌ PDF-Layout vorbereiten und testen  

---

### 7. Marketing-Homepage
❌ SEO-optimierte Homepage erstellen  
❌ Kontaktformular / Newsletter-Anmeldung implementieren  
❌ Responsive Design (Desktop, Tablet, Mobile)  
❌ Echtzeit-Elemente via WebSocket vorbereiten  
❌ Testing: Jest + React Testing Library  

---

### 8. Backend & Infrastruktur
❌ Python FastAPI Backend aufsetzen  
❌ Authentifizierung & Autorisierung implementieren  
❌ REST API vorbereiten  
❌ WebSocket-Server einrichten  
❌ Elasticsearch für Suche einrichten  
❌ Redis Caching implementieren  
❌ Celery + RabbitMQ für Hintergrundjobs einrichten  
❌ Deployment vorbereiten: Docker + AWS ECS / Kubernetes  
❌ CI/CD via GitHub Actions  

---

### 9. Frontend (Flutter & Web/Admin)
❌ Mobile App: Flutter (Dart) implementieren  
❌ State Management: Riverpod / Provider einrichten  
❌ Routing: go_router implementieren  
❌ HTTP Client: dio einrichten  
❌ JSON Serialisierung: json_serializable vorbereiten  
❌ Rich Text Editor: flutter_quill / zefyr einbauen  
❌ Web/Admin Panel: React + Next.js aufsetzen  
❌ Styling: TailwindCSS / Styled Components implementieren  
❌ Formularhandling: React Hook Form / Formik implementieren  
❌ SEO: next-seo implementieren  

---

## Architekturübersicht

### Backend & Infrastruktur
- Programmiersprache: Python 3.11+
- Framework: FastAPI
- Auth: fastapi-jwt-auth
- ORM & Datenbanken: SQLAlchemy (PostgreSQL), MongoDB (motor)
- Suche: Elasticsearch (elasticsearch-py)
- Caching: Redis
- WebSocket-Support für Echtzeitkommunikation
- Hintergrundjobs: Celery + RabbitMQ
- Export-Services & Moderationstools

### Frontend
- Mobile App: Flutter (Dart)
  - State Management: Riverpod oder Provider
  - Rich Text Editor: flutter_quill oder zefyr
  - Routing: go_router
  - WebSocket: web_socket_channel oder socket_io_client
  - HTTP Client: dio
  - JSON Serialisierung: json_serializable
- Web / Admin Panel: React + Next.js
  - Styling: TailwindCSS / Styled Components
  - Formularhandling: React Hook Form / Formik
  - SEO: next-seo
  - Testing: Jest + React Testing Library

### Infrastruktur & Deployment
- Hosting Frontend App: AWS S3 + CloudFront
- Hosting Marketing-Webseite: Vercel / Netlify
- Backend Deployment: Docker + AWS ECS / Kubernetes
- CI/CD: GitHub Actions

---

## Feature-Struktur & Module

### Frontend (Flutter)
- Auth & User Profil
- Notiz-Editor
- Hadith & Ayat Integration
- Community Feed & Gruppen
- Chat, Benachrichtigungen & Einstellungen
- Export-Funktion

### Frontend (React Web/Admin)
- Web-Admin Panel
- Erweiterte Community Features & Moderation
- Statistiken & Analytics Dashboard

### Backend (Python)
- REST API
- WebSocket Server
- Authentifizierung & Autorisierung
- Hadith & Ayat Datenbankmanagement & Suche
- Export Services
- Moderation & Admin Tools

---

## Datenbanken & Caching
- PostgreSQL / MongoDB
- Elasticsearch
- Redis für Caching

---

## Real-Time & Kommunikation
- WebSocket über socket_io_client oder web_socket_channel
- Echtzeit-Chat und Benachrichtigungen

---

## Autor
Tullab Al-Ilm Team
