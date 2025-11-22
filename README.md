## To repozytorium zawiera dokumentację również w języku polskim, która znajduje się poniżej.

# EN / REST API – Pokémon Data Fetching System

This project is a collection of small web applications organized within a single repository. Each module represents a standalone system with its own logic, styling, and PHP backend.

# 🚀 Features

    1. "sPrzychodni"

        A simple web form application used for submitting data (likely related to clinic or appointment handling). Includes:

            •	A frontend form (fromprzych.html)
            •	Backend request handler (receive.php)
            •	Dedicated stylesheet (style.css)

    2. "sGlosowania"

        A role-based voting system with separate interfaces and functionalities for three user types:

            •	User: submits votes
            •	Admin: manages the voting process and system configuration
            •	Secretary: generates PDFs and handles administrative exports

        Includes features such as:

            •	Login and logout mechanism
            •	Voting submission
            •	Administrative tools
            •	PDF processing
            •	Custom styles for each module

# 📋 Requirements

## Functional Requirements
	1. General

        •	The system must allow different web modules (applications) to operate independently.
        •	Each module must have access to Composer autoloading via the vendor/ directory.

    2. sPrzychodni

        •	The user must be able to open and submit a form.
        •	Submitted data must be sent to the backend (receive.php).
        •	The backend must correctly process and respond to user input.
        •	Styling must be applied through style.css.

    3. sGlosowania

        - Authentication

            •	Users must be able to log in and log out through PHP-based sessions.
            •	Unauthorized users must not access protected pages.

        - Voting (dlaUsera)

            •	A logged-in user must be able to cast a vote.
            •	Votes must be processed by the backend (obslugaGlosu.php).

        - Admin Panel (dlaAdmina)

            •	Admins must be able to access system settings.
            •	Admins must be able to manage voting configuration.
            •	The admin handler (obslugaAdmin.php) must process admin actions.

        - Secretary Panel (dlaSekretarza)

            •	Secretaries must be able to access the secretary dashboard.
            •	The system must allow generating PDFs through obslugaPDF.php.
            •	Administrative tasks must be handled via obslugaSekretarz.php.

## Non-Functional Requirements
    1. Security

        •	Login-protected modules must secure access using PHP sessions.
        •	Sensitive operations (admin, secretary) should only be accessible to authorized users.

    2. Maintainability

        •	Composer autoloading must support reusable classes and scalable code structure.
        •	Each module must remain isolated to simplify debugging and expansion.

    3. Performance

        •	Backend operations should be lightweight and optimized for small hosting environments.
        •	PDF generation should be efficient and not overload the server.

    4. Usability

        •	Each module must include clear navigation and simple UI (HTML + CSS).
        •	Role-based interfaces must be intuitive for non-technical users.

# 🧩 Architecture

The project follows a modular PHP architecture, organized into independently functioning web applications under a shared repository.

## Architectural characteristics:
	•	Modular structure: each app has its own folders, PHP logic, and styling.
	•	Composer-based autoloading: shared vendor folder ensures consistent namespace handling.
	•	Role-based separation: in sGlosowania, logic is split per user type (Admin, User, Secretary).
	•	Server-side processing: PHP scripts handle all inputs and operations.
	•	Frontend static assets: each module includes its own CSS and HTML views.

# 🔧 Technologies
	•	PHP: primary backend technology for handling business logic
	•	Composer: dependency management and autoloading
	•	HTML: frontend structure for forms and interfaces
	•	CSS: styling for each sub-application
	•	PDF Processing: via PHP, used in the secretary module
	•	Sessions: user authentication and access control

**────────────────────────**

# PL / REST API – System Pobierania i Obsługi Małych Aplikacji Webowych

To repozytorium zawiera zestaw niewielkich aplikacji webowych, zorganizowanych w jednym projekcie. Każdy moduł działa jako oddzielna aplikacja posiadająca własną logikę, stylowanie i backend PHP.

# 🚀 Funkcje

    1. "sPrzychodni"

        Prosta aplikacja formularzowa służąca do przesyłania danych (prawdopodobnie związanych z obsługą przychodni lub formularzy zgłoszeniowych). W skład modułu wchodzą:

            •	Formularz frontendowy (fromprzych.html)
            •	Skrypt backendowy obsługujący dane (receive.php)
            •	Dedykowany plik stylów (style.css)

    2. "sGlosowania"

        System głosowania z podziałem na role użytkowników i oddzielnymi interfejsami dla każdej z nich:

            •	Użytkownik: oddaje głos
            •	Administrator: zarządza procesem głosowania i konfiguracją
            •	Sekretarz: generuje pliki PDF i zarządza dokumentami

        Moduł obejmuje:

            •	Mechanizm logowania i wylogowywania
            •	Obsługę głosowania
            •	Funkcje administracyjne
            •	Generowanie PDF
            •	Oddzielne style dla każdego elementu systemu


# 📋 Wymagania

## Wymagania funkcjonalne
	1. Ogólne

        •	System musi umożliwiać działanie osobnych modułów webowych niezależnie od siebie.
	    •	Każdy moduł musi mieć dostęp do autoloadingu Composer poprzez katalog vendor/.

    2. sPrzychodni

	    •	Użytkownik musi mieć możliwość otwarcia i wysłania formularza.
	    •	Dane z formularza muszą trafiać do backendu (receive.php).
	    •	Backend musi poprawnie przetworzyć i obsłużyć przesłane informacje.
	    •	Stylowanie formularza musi być nadawane poprzez style.css.

    3. sGlosowania

        - Autoryzacja

        	•	Użytkownicy muszą móc logować się i wylogowywać za pomocą sesji PHP.
        	•	Strony chronione muszą blokować dostęp osobom nieuprawnionym.

        - Głosowanie (dlaUsera)

	        •	Zalogowany użytkownik musi mieć możliwość oddania głosu.
	        •	Głosy muszą być przetwarzane przez backend (obslugaGlosu.php).

        - Panel Administratora (dlaAdmina)

	        •	Administrator musi mieć dostęp do ustawień systemu.
	        •	Administrator musi móc zarządzać procesem głosowania.
	        •	Logika admina musi być obsługiwana przez obslugaAdmin.php.

        - Panel Sekretarza (dlaSekretarza)

        	•	Sekretarz musi mieć dostęp do panelu sekretarza.
        	•	System musi umożliwiać generowanie plików PDF (obslugaPDF.php).
        	•	Zadania sekretarza muszą być realizowane przez obslugaSekretarz.php.

 ## Wymagania niefunkcjonalne
    1. Bezpieczeństwo

        •	Chronione moduły muszą używać sesji PHP do zabezpieczenia dostępu.
        •	Wrażliwe funkcje (administrator, sekretarz) muszą być ograniczone tylko do uprawnionych użytkowników.

    2. Utrzymywalność

        •	Autoloading Composer musi wspierać możliwość ponownego wykorzystania klas i rozbudowy projektu.
        •	Moduły powinny być odseparowane, aby ułatwić debugowanie i dalszy rozwój.

    3. Wydajność

        •	Operacje backendowe powinny być lekkie i dostosowane do małych serwerów hostingowych.
        •	Generowanie PDF musi być szybkie i nie może przeciążać zasobów serwera.

    4. Użyteczność

        •	Każdy moduł powinien mieć prostą i przejrzystą nawigację.
        •	Interfejsy oparte na rolach muszą być łatwe do zrozumienia dla użytkowników nietechnicznych.

# 🧩 Architektura

Projekt wykorzystuje modularną architekturę PHP, w której każda aplikacja webowa działa niezależnie, korzystając z wspólnego repozytorium.

## Charakterystyka architektury:
	•	Struktura modułowa: każda aplikacja posiada własne foldery, logikę oraz pliki styli
	•	Autoloading Composer: wspólny katalog vendor/ zapewnia obsługę klas i przestrzeni nazw
	•	Podział na role: moduł „sGlosowania” rozdziela logikę dla Admina, Użytkownika i Sekretarza
	•	Przetwarzanie po stronie serwera: wszystkie dane są obsługiwane przez skrypty PHP
	•	Statyczne zasoby frontendowe: każdy moduł posiada własne pliki HTML i CSS

# 🔧 Technologie
	•	PHP: obsługa logiki biznesowej i backend
	•	Composer: autoloading oraz zarządzanie zależnościami
	•	HTML: struktura interfejsów i formularzy
	•	CSS: stylowanie modułów i podstron
	•	Generowanie PDF – funkcjonalność panelu sekretarza
	•	Sesje PHP – logowanie, wylogowywanie i ochrona treści
