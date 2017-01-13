# Public Maps

Główne repozytorium publicznych map dla pluginu [Arcade 2](https://github.com/ShootGame/Arcade2).

Wszystkie pliki tekstowe powinny posiadać znak końca linii `LF` - `git config core.autocrlf true`.
Repozytorium ignoruje foler `test/`.
Repozytorium składa się z folderów które reprezentują repozytoria map dla pluginu Arcade.

- Każdy folder mapy - ze względu na ograniczenia systemowe - powinien posiadać: `A-Z`, `a-z`, `0-9`, `-`, `_`, ` `.
- Każda mapa powinna posiadać plik `map.xml` z jej konfiguracją. Niedopusczalny jest brak tego pliku w `production`.
- Każda mapa instalowana w `production` powinna zostać przetestowana w `development` pod względem konfiguracji oraz gry.

***

### `production/`

Repozytorium map gotowych do odtworzenia przez serwery produkcyjne.

- Plik `map.xml` nie może posiadać **jakichkolwiek** błędów.
- Mapa nie może zawierać błędów, szczególnie tych wpływających na grę.
- Mapa powinna być ograniczona wyłącznie do niezbędnych chunków mapy.
- Świat mapy powinien zostać ograniczony do plików `level.dat`, `region/` oraz przy potrzebie także `data/`.

***

### `development/`

Repozytorium map testowych do odtworzenia przez serwery testowania map.

- To repozytorium nie jest brudnopisem - powinno zawierać jedynie mapy testowe.
- Mapa musi zawierać plik `map.xml`.
- Plik `map.xml` musi zawierać przynajmniej podstawową konfigurację.
