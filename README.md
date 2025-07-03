# Gerzhan template monorepo

[github.com/gerzhan/gerzhan-tpl-turbo-start](https://github.com/gerzhan/gerzhan-tpl-turbo-start)

## Описание

Репозиторий для быстрого запуска проекта в виде моногрепозитория.
Базовый код репозитория сгенерирован соглано инструкции [ui.shadcn.com/docs/monorepo](https://ui.shadcn.com/docs/monorepo)

```bash
# начальная команда генерации данного репозитория
$pnpm dlx shadcn@canary init
```

## Порядок добавления components

Компоненты `shadcn` добавляются отдельно для каждого приложении в `apps`:

```bash
# пример добавления компонента в apps/web из корневой директории монорепозитория
$pnpm dlx shadcn@latest add button -c apps/web
```

В результате компонент будет размещен в директории `packages/ui/src/components`.

## Tailwind

В `tailwind.config.ts` и `globals.css` сконфигурированы на использование `packages/ui` .

## Использование components

В каждом приложение подключение (доступ) `ui` package осуществляется через импорт.

```tsx
import {Button} from '@gerzhan/ui/components/button';
import {useTheme} from '@gerzhan/ui/hooks/use-theme';
import {cn} from '@gerzhan/ui/lib/utils';
```

## TODO

- [blocks registry](https://ui.shadcn.com/docs/blocks)
