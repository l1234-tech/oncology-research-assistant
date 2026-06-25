# AI Research Assistant — Onkology track

## Что это
Мультиагентная система-помощник для врачей-онкологов и исследователей. 
Ищет, оценивает и синтезирует научную информацию из реальных медицинских баз данных.

## Архитектура
- **Researcher** — поиск источников (PubMed, ClinicalTrials.gov, локальная база PDF)
- **Critic** — оценка качества и релевантности найденного
- **Synthesizer** — структурированный финальный ответ

## Установка
1. `python3 -m venv venv && source venv/bin/activate`
2. `pip install -r requirements.txt`
3. Создать `.env` с переменной `GEMINI_API_KEY`
4. Положить PDF научных статей в `docs/`
5. Запустить индексацию: `python index.py`
6. Запустить агента: `python chat.py`

## Стек
Python 3.11, Google Gemini API, sentence-transformers, SQLite, PubMed E-utilities, ClinicalTrials.gov API