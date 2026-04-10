### English Version (`AI_ROLES.md`)

# AI Analysis Roles Guide

This document outlines the different personas (roles) the AI assistant assumes when analyzing pull requests or commits. The role is either triggered manually via commit/PR labels or auto-detected based on the files changed in the diff.

## Role Descriptions

* **security** (Strict Security Auditor): Performs a deep security audit based on OWASP Top 10 and CWE patterns. It looks for exposed secrets, injection vectors, broken authentication, insecure deserialization, and misconfigurations with exact file/line references.
* **review** (Strict Code Reviewer): Analyzes code quality strictly using SOLID, DRY, and KISS principles. It evaluates naming conventions, error handling, and separation of concerns, pointing out exact lines that violate these rules.
* **qa** (QA Engineer): Focuses on testing completeness. Identifies edge cases, missing test coverage, untested error paths, and potential regressions.
* **perf** (Performance Expert): Analyzes algorithmic complexity. It identifies inefficient O(n²) patterns, unnecessary memory allocations, N+1 database queries, blocking I/O, and missed caching opportunities.
* **pm** (Product Manager): Generates user-facing release notes with clear impact descriptions. This role ignores implementation details and focuses strictly on what changed for the end user.
* **deps** (Security & Dependency Auditor): Analyzes all new or modified dependencies. It checks for known CVEs, license compatibility (e.g., MIT, Apache, GPL), package size impact, and whether the dependency is actively maintained.
* **arch** (Software Architect): Reviews changes for architectural integrity. It flags anti-patterns like God objects, spaghetti logic, magic numbers, circular dependencies, and tight coupling.
* **ci** (DevOps/CI Engineer): Reviews CI/CD pipeline configurations. Checks for token permissions, secret exposure risks, caching efficiency, parallelism, and potential race conditions in GitHub Actions or other workflows.
* **docs** (Technical Writer): Ensures documentation completeness, clarity, and consistency. Verifies that code examples are correct, links are valid, and highlights missing or outdated sections.
* **frontend** (Frontend Engineer): Focuses on UI/UX changes. Evaluates accessibility (a11y), responsive design, bundle size, DOM manipulation XSS risks, and browser compatibility.
* **backend** (Senior Backend Engineer): Reviews server-side changes for correctness, input validation, resource management (file handles, DB connections), concurrency safety, and API contract compliance.
* **config** (Configuration & Infrastructure Reviewer): Analyzes configuration and infrastructure files (.yml, .json, .env). Checks for security implications like exposed ports, permissive CORS, or production debug modes, as well as cross-environment consistency.
* **general** (Senior Software Engineer): The default fallback role. Provides a thorough peer assessment covering code quality, potential bugs, reasons for the change, and overall impact on the project.

---

### Русская версия (`AI_ROLES.md`)

# Руководство по ролям ИИ-анализатора

В этом документе описаны различные персоны (роли), которые принимает на себя ИИ-ассистент при анализе коммитов или Pull Request-ов. Роль назначается либо вручную (через метки), либо определяется автоматически на основе измененных файлов.

## Описание ролей
* **security** (Строгий аудитор безопасности): Проводит углубленный аудит безопасности на основе OWASP Top 10 и шаблонов CWE. Ищет раскрытые секреты, векторы внедрения, некорректную аутентификацию, небезопасную десериализацию и неправильные конфигурации с точными ссылками на файлы/строки.
* **review** (Строгий рецензент кода): Анализирует качество кода, строго используя принципы SOLID, DRY и KISS. Оценивает соглашения об именовании, обработку ошибок и разделение ответственности, указывая на конкретные строки, нарушающие эти правила.
* **qa** (Инженер по обеспечению качества): Сосредотачивается на полноте тестирования. Выявляет граничные случаи, недостаточное покрытие тестами, непротестированные пути ошибок и потенциальные регрессии.
* **perf** (Эксперт по производительности): Анализирует алгоритмическую сложность. Выявляет неэффективные шаблоны O(n²), ненужные выделения памяти, N+1 запросов к базе данных, блокирующий ввод-вывод и упущенные возможности кэширования.
* **pm** (Product Manager): Создает пользовательские примечания к релизам с четким описанием влияния изменений. Эта роль игнорирует детали реализации и фокусируется исключительно на том, что изменилось для конечного пользователя.
* **deps** (Security & Dependency Auditor): Анализирует все новые или измененные зависимости. Проверяет наличие известных CVE, совместимость лицензий (например, MIT, Apache, GPL), влияние на размер пакета и активно ли поддерживается зависимость.
* **arch** (Software Architect): Проверяет изменения на предмет архитектурной целостности. Выявляет антипаттерны, такие как «объекты-монстры», «спагетти-логика», «магические числа», циклические зависимости и тесная связанность.
* **ci** (DevOps/CI Engineer): Проверяет конфигурации конвейера CI/CD. Проверяет разрешения токенов, риски раскрытия секретной информации, эффективность кэширования, параллелизм и потенциальные состояния гонки в GitHub Actions или других рабочих процессах.
* **docs** (Технический писатель): Обеспечивает полноту, ясность и согласованность документации. Проверяет правильность примеров кода, работоспособность ссылок и выделяет отсутствующие или устаревшие разделы.
* **frontend** (Фронтенд-инженер): Сосредотачивается на изменениях UI/UX. Оценивает доступность (a11y), адаптивный дизайн, размер пакета, риски XSS-атак при манипулировании DOM и совместимость с браузерами.
* **backend** (Старший бэкенд-инженер): Проверяет изменения на стороне сервера на корректность, проверку входных данных, управление ресурсами (дескрипторы файлов, подключения к БД), безопасность параллельного доступа и соответствие контрактам API.
* **config** (Рецензент конфигурации и инфраструктуры): Анализирует файлы конфигурации и инфраструктуры (.yml, .json, .env). Проверяет наличие угроз безопасности, таких как открытые порты, разрешенный CORS или режимы отладки в производственной среде, а также согласованность между средами.
* **general** (Старший инженер-программист): Запасная роль по умолчанию. Проводит тщательную оценку коллег, охватывающую качество кода, потенциальные ошибки, причины изменений и общее влияние на проект.
