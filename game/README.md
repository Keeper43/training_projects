## Задача:
По данным о событиях, совершённых в мобильной игре, проанализировать поведение пользователей. Также необходимо оценить эффективность рекламных источников.

## Что было сделано:
Проведена предобработка данных. Проведён когортный анализ. Рассчитаны метрики: DAU, WAU, MAU, Retention Rate, LTV, CAC, ROMI, построены графики. Сделаны выводы.

## Имеющиеся данные:
Датасет game_actions.csv:
Содержит данные о событиях пользователей, совершённые на первом уровне игры. Содержатся данные первых пользователей, которые начали пользоваться приложением с 4 по 10 мая включительно. Завершение первого уровня возможно двумя путями:
  1) Победа над первым врагом
  2) Реализация проекта разработки орбитальной сборки спутников
Основная монетизация игры только планируется и предполагается в виде показа рекламы на экране с выбором объекта постройки.
Данные:
  - event_datetime — время события;
  - event — одно из трёх событий:
     1. building — объект построен,
     2. finished_stage_1 — первый уровень завершён,
     3. project — проект завершён;
  - building_type — один из трёх типов здания:
     1. assembly_shop — сборочный цех,
     2. spaceport — космопорт,
     3. research_center — исследовательский центр;
  - user_id — идентификатор пользователя;
  - project_type — тип реализованного проекта;

Помимо основного, есть ещё 2 датасета с рекламными активностями:
1. Датасет ad_cost.csv:
  - day - день, в который был совершен клик по объявлению
  - source - источник трафика
  - cost - стоимость кликов
2. Датасет costs.csv:
  - user_id - идентификатор пользователя
  - source - источников, с которого пришёл пользователь, установивший приложение