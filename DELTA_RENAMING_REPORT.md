# Отчет о переименовании Paper в Delta

## Выполненные изменения

### 1. Основные файлы конфигурации

#### README.md
- ✅ Изменено название проекта с "Paper" на "Delta"
- ✅ Изменено описание с "Paperclip" на "Deltaclip"
- ✅ Обновлены ссылки на документацию
- ✅ Изменены примеры зависимостей Maven/Gradle с `paper-api` на `delta-api`
- ✅ Обновлены упоминания команды с `/paper` на `/delta`

#### gradle.properties
- ✅ Изменена группа с `io.papermc.paper` на `io.papermc.delta`

#### settings.gradle.kts
- ✅ Изменено название корневого проекта с "paper" на "delta"

#### build.gradle.kts
- ✅ Изменены координаты API с `paper-api` на `delta-api`
- ✅ Переименована задача с `printPaperVersion` на `printDeltaVersion`

### 2. Файлы плагинов

#### test-plugin/src/main/resources/delta-plugin.yml
- ✅ Переименован файл с `paper-plugin.yml` на `delta-plugin.yml`
- ✅ Изменено название плагина с "Paper-Test-Plugin" на "Delta-Test-Plugin"
- ✅ Изменено описание с "Paper Test Plugin" на "Delta Test Plugin"

### 3. Патчи сервера

#### Команды
- ✅ Изменена команда с `/paper` на `/delta` в патче `0017-Paper-command.patch`
- ✅ Обновлены разрешения с `bukkit.command.paper` на `bukkit.command.delta`
- ✅ Изменено описание команды с "Paper related commands" на "Delta related commands"
- ✅ Обновлена регистрация команды с "Paper" на "Delta" в нескольких патчах

#### Информация о версии
- ✅ Изменены заголовки манифеста в `0033-Expose-server-build-information.patch`:
  - Implementation-Title: "Paper" → "Delta"
  - Specification-Title: "Paper" → "Delta"
  - Specification-Vendor: "Paper Team" → "Delta Team"
  - Brand-Id: "papermc:paper" → "papermc:delta"
  - Brand-Name: "Paper" → "Delta"

#### API патчи
- ✅ Обновлен `0015-Expose-server-build-information.patch`:
  - BRAND_PAPER_ID: "papermc:paper" → "papermc:delta"
  - Обновлены комментарии и документация
  - Изменены примеры в Javadoc

### 4. Области, требующие дополнительного внимания

#### Не изменено (требует дополнительной работы):
1. **Папки проекта**: Paper-API и Paper-Server остались с оригинальными именами
2. **Пакеты Java**: `io.papermc.paper` остались без изменений
3. **Некоторые патчи**: Многие патчи содержат упоминания "Paper" в комментариях и коде
4. **GitHub Actions**: Файлы CI/CD содержат упоминания Paper
5. **Документация**: CONTRIBUTING.md и другие файлы документации

#### Рекомендации для полного переименования:

1. **Переименование папок проекта**:
   ```bash
   mv Paper-API Delta-API
   mv Paper-Server Delta-Server
   ```

2. **Обновление пакетов Java**:
   - Изменить `io.papermc.paper` на `io.papermc.delta`
   - Обновить все импорты в коде

3. **Обновление GitHub Actions**:
   - Изменить названия workflow'ов
   - Обновить ссылки на репозиторий

4. **Массовое обновление патчей**:
   - Использовать скрипт для замены всех упоминаний "Paper" на "Delta" в патчах
   - Исключить технические термины и ссылки на внешние ресурсы

5. **Обновление документации**:
   - CONTRIBUTING.md
   - LICENSE.md
   - Другие файлы документации

## Заключение

Выполнены основные изменения для переименования визуальных элементов Paper в Delta. Команды теперь работают как `/delta` вместо `/paper`, а сервер будет отображаться как "Delta" в сообщениях о версии. Для полного переименования потребуется дополнительная работа с пакетами Java и массовым обновлением патчей. 