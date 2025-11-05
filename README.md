# Spotifum — OOP Project

Grade: 17 / 20 ⭐

## Short description

Spotifum is an academic OOP project that simulates basic music player features and management of users, playlists, and reproductions. The codebase is organized into Java packages that handle music, playlists, users, reproductions, and query/report generation.

## Main features

- Music management (create, read)
- User management and subscription plans
- Public/private playlists, generated playlists, and favorites
- Reproduction management (logging, counters)
- Queries/reports (most played music, most listened interpreter, etc.)

## Requirements

- Java 21 (recommended)
- Gradle (the repository includes the wrappers `gradlew` / `gradlew.bat`)

## Build & run

Using the included wrapper (recommended):

```bash
./gradlew build
```

After the build finishes, run the generated JAR (name may vary — check `build/libs`):

```bash
java -jar build/libs/spotifum-1.0-SNAPSHOT.jar
```

## Repository structure

Key folders (relative to project root):

- `src/main/java/spotifum/`

  - `Musics/` — classes and interfaces related to music (e.g., `Musica`, `MusicManager`)
  - `Playlists/` — playlists, playlist generators, and playback management
  - `Users/` — user management and subscription plans
  - `Reproductions/` — reproduction records and manager
  - `Menu/` — console interaction classes (input/menu handling)
  - `queries/` — system queries and reporting utilities
  - `Exceptions/` — custom exceptions (e.g., `MusicNotFoundException`)

- `src/test/java/spotifum/` — unit tests organized by package (Musics, Playlists, Users, etc.)

## State files

The project includes an initial state folder `Load_States/Estado1/` with `.ser` files (serialized objects). These files are used to populate the system with example data at startup.

## UML diagram

The project's UML diagram is available at `Diagrama UML - POO.png` in the repository root. It provides a quick overview of the main classes and relationships.

## Running tests locally

To run all JUnit tests:

```bash
./gradlew test
```