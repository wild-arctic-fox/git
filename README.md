# git
git-flow — это набор расширений git предоставляющий высокоуровневые операции над репозиторием для поддержки модели ветвления

## Master Branches  -  хранит официальную историю релизов.
## Develop Branches  - служит ветвью интеграции для функций.
----
**Просмотр веток**
```
git branch
```
**Создание ветки 'develop'**
```
git branch develop
```
**Дополнение main/master ветки**
```
git push -u origin develop
```
**Инициализация git flow**
```
git flow init
git branch * develop  master
```

## Feature Branches  
  - Каждая новая функция должна находиться в отдельной ветке. 
  - Когда функция завершена, она снова включается в разработку. 
  - Нет прямого взаимодействия  с мастером.

**Это действие создаёт новую ветку фичи, основанную на ветке "develop", и переключается на неё.**
```
git flow feature start feature_branch_1
```
**Слияние ветки feature_branch_1 в "develop".
Удаление ветки фичи.
Переключение обратно на ветку "develop."**
```
git flow feature finish feature_branch_1
```
## Release Branches
  - Поддержка подготовки нового релиза продукта
  - Позволяет устранять мелкие баги и подготавливать различные метаданные для релиза (+документация)

```
git flow release start 0.1.0
git flow release finish '0.1.0'
```
