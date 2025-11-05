# Spotifum — Projeto POO

Spotifum é um projecto académico (POO) que simula funcionalidades básicas de um reprodutor de música e gestão de utilizadores, playlists e reproduções. O código está organizado em pacotes Java com funcionalidades para gerir músicas, playlists, reproduções e consultas/relatórios.

Grade: 17 / 20 ⭐

## Principais funcionalidades

- Gestão de músicas (criação, leitura)
- Gestão de utilizadores e planos de subscrição
- Playlists públicas/privadas, playlists geradas e favoritas
- Gestão de reproduções (registo, contadores)
- Queries/relatórios (música mais reproduzida, intérprete mais ouvido, etc.)

## Requisitos

- Java 21 (recomendado)
- Gradle (o repositório inclui wrappers `gradlew`/`gradlew.bat`)

## Build e execução

Usando o wrapper incluído (recomendado):

```bash
./gradlew build
```

Depois de construir, execute o JAR gerado (o nome pode variar, use o ficheiro em `build/libs`):

```bash
java -jar build/libs/spotifum-1.0-SNAPSHOT.jar
```

## Estrutura do repositório

Resumo das pastas mais importantes (caminho relativo ao projecto):

- `src/main/java/spotifum/`

  - `Musics/` — classes e interfaces relacionadas com músicas (e.g., `Musica`, `MusicManager`)
  - `Playlists/` — playlists, geradores de playlists e gestão de reprodução
  - `Users/` — gestão de utilizadores e planos de subscrição
  - `Reproductions/` — registos de reprodução e manager associado
  - `Menu/` — classes para interacção em consola (input/menus)
  - `queries/` — classes com queries e relatórios do sistema
  - `Exceptions/` — excepções customizadas (e.g., `MusicNotFoundException`)

- `src/test/java/spotifum/` — testes unitários organizados por pacotes (Musics, Playlists, Users, etc.)

## Ficheiros de estado

O projecto inclui um directório de estados iniciais `Load_States/Estado1/` com ficheiros `.ser` (objetos serializados). Estes são usados para popular o sistema com dados de exemplo durante o arranque.

## Diagrama UML

O diagrama UML do projecto encontra-se em `Diagrama UML - POO.png` (raiz do repositório). Consulte-o para uma visão rápida das principais classes e relações.

## Executar testes localmente

Para executar todos os testes JUnit:

```bash
./gradlew test
```