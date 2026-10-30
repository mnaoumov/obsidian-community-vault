---
title: 'База знаний сообщества "Obsidian Чат"'
aliases:
  - 'База знаний сообщества "Obsidian Чат"'
linter-yaml-title-alias: 'База знаний сообщества "Obsidian Чат"'
---

# База знаний сообщества "Obsidian Чат"

![](<./!!files/logo.jpg>)

Это база знаний в формате хранилища [Obsidian](http://obsidian.md/) русскоговорящего Telegram-сообщества [Obsidian Чат](https://t.me/obsidian_z).

Локально выкачать себе эту базу можно из репозитория <https://github.com/mnaoumov/obsidian-community-vault>

Можно предлагать свои правки прямо на сайте репозитория, либо стандартными механизмами GitHub Fork / Pull Request, которые требуют [небольшого знакомства с Git](<./Добавление изменений в базу на GitHub.md>).

## Важно

- В настройках Obsidian выключены Wiki-ссылки и настроены относительные ссылки для лучшей переносимости хранилища между различными платформами.
- В хранилище включен и настроен плагин [Linter](<./Плагины/Linter.md>), которым нужно форматировать все изменения (`Ctrl + S`).

## Filing an issue (for AI agents and humans)

Open issues through the [issue forms](https://github.com/mnaoumov/obsidian-community-vault/issues/new/choose), not as blank issues.

Filing from the CLI or the API (`gh issue create --body`, or an AI agent filing for you) skips the form, and `gh issue create --template` cannot load an issue form. In that case, open the matching form in [`.github/ISSUE_TEMPLATE/`](https://github.com/mnaoumov/obsidian-community-vault/tree/HEAD/.github/ISSUE_TEMPLATE), copy every field as a `### <label>` heading in the form's order, and fill in each one. Always state the version you used and your operating system.
