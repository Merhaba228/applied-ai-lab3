# Лабораторная работа №3

## Запуск

```bash
python src/prepare_data.py
```

## Запуск через DVC

```bash
python -m dvc repro
python -m dvc status
```

Скрипт читает исходный архив, выполняет очистку и сохраняет `data/processed/nyc_taxi_clean.csv`.
Большой датасет отслеживается DVC, а код и настройки можно хранить в Git.
