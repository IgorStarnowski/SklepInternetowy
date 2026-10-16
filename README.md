# 🛒 Sklep Internetowy (Spring Boot)

Prosta aplikacja webowa realizująca podstawowe funkcjonalności platformy e-commerce. Projekt został napisany w języku **Java** z wykorzystaniem frameworka **Spring Boot**. Architektura aplikacji opiera się na wzorcu **MVC (Model-View-Controller)**, a interfejs użytkownika generowany jest po stronie serwera przy pomocy silnika szablonów **Thymeleaf**.

## ✨ Główne funkcjonalności

* **Katalog produktów:** Przeglądanie dostępnego asortymentu na stronie głównej.
* **Obsługa koszyka:** Możliwość dodawania produktów do koszyka zakupowego oraz podgląd jego zawartości i wartości całkowitej.
* **Realizacja zamówień:** Proces składania zamówienia, zapisywanie danych o zamówionych pozycjach (`OrderItem`) oraz podsumowanie transakcji.
* **Panel Administratora:** Dedykowany widok umożliwiający dodawanie nowych produktów do bazy danych sklepu.
* **Inicjalizacja danych:** Automatyczne zasilenie bazy danych początkowym asortymentem przy starcie aplikacji (klasa `DbInit`).

## 🛠️ Zastosowane technologie

* **Język programowania:** Java
* **Główny framework:** Spring Boot (Spring Web)
* **Dostęp do danych:** Spring Data JPA / Hibernate
* **Baza danych:** H2 Database (w pamięci)
* **Frontend:** HTML5, CSS3, Thymeleaf
* **Budowanie i zależności:** Maven (Maven Wrapper)

## 📂 Struktura projektu

Projekt zachowuje standardowy podział warstwowy dla aplikacji Spring Boot:

* `controller/` – klasy obsługujące żądania HTTP (np. `HomeController`, `OrderController`, `AdminController`).
* `service/` – warstwa logiki biznesowej (np. `CartService`, `OrderService`).
* `repository/` – interfejsy komunikujące się z bazą danych (Spring Data JPA).
* `model/` – klasy encyjne odwzorowujące tabele w bazie danych (np. `Item`, `Order`, `Cart`).
* `dto/` – obiekty transferu danych (Data Transfer Objects).
* `resources/templates/` – widoki HTML oparte na znacznikach Thymeleaf.
* `resources/static/` – pliki statyczne (arkusze stylów CSS).

## ⚙️ Wymagania wstępne

Aby uruchomić aplikację, upewnij się, że posiadasz zainstalowane w systemie:
* **Java Development Kit (JDK)** w wersji 11 lub nowszej (rekomendowana 17+).
* **Środowisko IDE** (np. IntelliJ IDEA, Eclipse) – opcjonalnie.

## 🚀 Uruchomienie lokalne

Projekt korzysta z narzędzia **Maven Wrapper**, co oznacza, że nie musisz mieć zainstalowanego Mavena globalnie w systemie.

1. Sklonuj repozytorium na swój dysk lokalny:

       git clone https://github.com/IgorStarnowski/SklepInternetowy.git

2. Przejdź do głównego katalogu projektu (tam, gdzie znajduje się plik `pom.xml`):

       cd SklepInternetowy

3. Zbuduj i uruchom aplikację wpisując poniższe polecenie:

   * **Windows:**

         mvnw.cmd spring-boot:run

   * **Linux/macOS:**

         ./mvnw spring-boot:run

4. Po poprawnym uruchomieniu wbudowanego serwera Tomcat, otwórz przeglądarkę i przejdź pod adres:
   👉 `http://localhost:8080`

*(Alternatywnie aplikację można zaimportować jako projekt Maven do środowiska IDE i uruchomić bezpośrednio z poziomu głównej klasy `SklepApplication.java`).*
