# Проект: Маркетинг

## Краткое описание
Проект по прогнозированию бинарного целевого признака с существенным дисбалансом классов (2% положительных случаев).

Основные особенности проекта:
1. Для заполнения пропусков была использована модель DecisionTreeClassifier / Regressor.
2. Для оценки важности признаков была использована модель RandomForestClassifier.
3. Для решения проблемы сильного дисбаланса классов (2% положительных случаев) применена комбинированная стратегия SMOTETomek, сочетающая синтетическую генерацию примеров миноритарного класса (SMOTE) и очистку данных от шумовых наблюдений (Tomek Links).
4. Учитывая отсутствие сильной линейной зависимости между признаками и целевой переменной, выбор был сделан в пользу ансамблевых методов, показавших лучшие результаты на нелинейных зависимостях.
5. В процессе моделирования тестировались четыре алгоритма: LightGBM, Random Forest, Logistic Regression и SVM, с оптимизацией по метрике ROC-AUC.

Лучший результат показала модель LightGBM со следующими характеристиками:
- ROC-AUC = 72%;
- Оптимальный порог классификации: 0.74;
- Accuracy: 0.74;
- Precision: 0.05;
- Recall: 0.61.

Полученная модель демонстрирует приемлемую предсказательную способность.

## Структура проекта
```
Masterskaya_marketing
├── data/ # данные для обучения (скрыты)
├── .gitignore
├── README.md   # описание проекта
└── Marketing_workbook.ipynb # исследование проекта и обучение моделей
```
## Контакты
 * Автор: Мироненко Денис
 * Email: denmironenko@gmail.com
