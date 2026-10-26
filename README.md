# QAI-07 - Домашнее задание

## Что находится в проекте

В проекте 4 основных файла:

```text
qai07_homework_final/
├── agent_instruction.md
└── skills/
    ├── requirement-review/
    │   └── SKILL.md
    ├── task-design/
    │   └── SKILL.md
    └── test-design/
        └── SKILL.md
```

## Что это такое

`agent_instruction.md` - общая инструкция для QA-агента:
- кто он;
- за что отвечает;
- что ему можно и нельзя;
- в каком порядке он работает;
- какие Quality Gates проверяет;
- когда должен остановиться и запросить человека.

`requirement-review/SKILL.md` - методика анализа требований:
- противоречия;
- неоднозначности;
- полнота;
- тестируемость;
- вопросы на уточнение.

`task-design/SKILL.md` - методика проектирования Jira-задач:
- название;
- описание;
- Acceptance Criteria;
- связь с требованиями;
- зависимости и открытые вопросы.

`test-design/SKILL.md` - методика проектирования тестовой модели для Qase:
- позитивные сценарии;
- негативные сценарии;
- граничные значения;
- роли и права;
- состояния и переходы;
- трассируемость к требованиям и Jira-задачам.

## Как открыть в IntelliJ IDEA

1. Распакуй архив.
2. Открой IntelliJ IDEA.
3. Нажми `File -> Open`.
4. Выбери папку `qai07_homework_final`.
5. Нажми `Open`.

Никакой Java, Maven, Gradle или Python для этой домашней работы не требуется.

Все файлы - обычный Markdown.

## Что проверить перед сдачей

Открой по очереди:

1. `agent_instruction.md`
2. `skills/requirement-review/SKILL.md`
3. `skills/task-design/SKILL.md`
4. `skills/test-design/SKILL.md`

Убедись, что понимаешь общий flow:

```text
Требования
   ↓
requirement-review
   ↓
Requirement Quality Gate
   ↓
task-design
   ↓
Task Design Quality Gate
   ↓
test-design
   ↓
Test Design Quality Gate
   ↓
Итоговый результат
```

Если требования содержат критические противоречия или данных недостаточно,
агент не должен ничего придумывать и продолжать зависимые этапы.

## Как это объяснить преподавателю

Коротко:

> Я спроектировал QA Orchestrator и три переиспользуемых Skill.
> Agent Instruction отвечает за общую оркестрацию, Scope, Tools,
> Quality Gates, Failure Behaviour и Escalation Rules.
> Каждый Skill отвечает только за одну компетенцию:
> review требований, проектирование Jira-задач или test design для Qase.
> При критической проблеме workflow блокируется и передается человеку.

## Что сдавать

Минимально:

- `agent_instruction.md`
- `skills/requirement-review/SKILL.md`
- `skills/task-design/SKILL.md`
- `skills/test-design/SKILL.md`

Если преподаватель просит ссылку:
- загрузи проект в GitHub;
- либо приложи/передай ссылку способом, указанным на платформе курса.

## Важно

Не нужно:
- писать Java-код;
- делать Maven-проект;
- подключать GigaChat API;
- делать Spring Boot;
- делать Artifact Contract для этой версии домашнего задания;
- создавать реальный агентный runtime.

На текущем этапе задача - именно проектирование Agent Instruction и Skills.
