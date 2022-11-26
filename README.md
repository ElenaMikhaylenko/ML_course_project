# Машинное обучение в бизнесе

## Итоговый проект

#### Стек:

ML: sklearn, pandas, numpy
API: flask


#### Данные: с kaggle - https://www.kaggle.com/rashikrahmanpritom/heart-attack-analysis-prediction-dataset

#### Задача: Анализ и прогноз сердечного приступа

#### Модель ML: Catboost

#### Клонируем репозиторий и создаем образ
```
$ git clone https://github.com/ElenaMikhaylenko/ML_course_project.git
$ cd ML_course_project
$ docker build -t app/ml_course_project/
```

#### Запускаем контейнер
Здесь Вам нужно создать каталог локально и сохранить туда предобученную модель (<your_local_path_to_pretrained_models> нужно заменить на полный путь к этому каталогу)

Предобученная модель лежит в ML_course_project/app/sv_pipeline.dill

```
$ docker run -d -p 8180:8180 -p 8181:8181 -v <your_local_path_to_pretrained_models>:/app/app/models app/ml_course_project/
```

#### Переходим на localhost:8181



