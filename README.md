# Лабораторная работа №3

## Запуск

Для запуска нужен Python и Git LFS.

```bash
git lfs install
git clone https://github.com/Merhaba228/applied-ai-lab3.git
cd applied-ai-lab3
git lfs pull
pip install -r requirements.txt
python -m dvc repro
```

Скрипт читает исходный архив, выполняет очистку и сохраняет `data/processed/nyc_taxi_clean.csv`.

## Почему архив есть в репозитории

По смыслу DVC тяжёлые данные должны храниться отдельно от Git. Но для учебной работы архив добавлен через Git LFS, чтобы проект можно было клонировать и запустить без отдельной настройки хранилища.

Архив не хранится как обычный текстовый файл Git. DVC-файл `data/raw/nyc-taxi-trip-duration.zip.dvc` и `dvc.lock` оставлены для демонстрации версионирования данных.

После настройки отдельного DVC-хранилища архив можно убрать из Git LFS и получать командой `dvc pull`.
