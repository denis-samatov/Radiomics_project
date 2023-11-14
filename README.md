# Методы машинного обучения в радиомике для анализа кардиоваскулярных изображений

---

## Abstract
This article outlines the idea of applying machine learning techniques in nuclear medicine to analyze cardiovascular images. The work includes segmentation of the affected area of the heart on the polar map, isolation of radiomic indicators from the ROI, and classification of patients into healthy individuals and patients with abnormalities. The article also presents some of the results of the initial study and the first stage of work.

---

## Введение
Радиомика представляет собой относительно молодую область радиологии, целью которой является извлечение количественных признаков из медицинских изображений. Методы машинного обучения и искусственного интеллекта, в сочетании с радиомикой, позволяют не только извлекать численные характеристики, но и обрабатывать большие объемы данных, что затруднительно традиционными методами.

В данной работе рассматривается применение радиомики и методов машинного обучения для анализа изображений, полученных методом перфузионной сцинтиграфии миокарда. Цель работы - создание математической модели для анализа тканей миокарда на основе радиомических признаков.

---

## Экспериментальная часть
В ходе работы была проведена сегментация области сердца на полярной карте, выделение радиомических показателей из области интереса (ROI) и классификация пациентов на здоровых и с патологиями. Использовались методы машинного обучения, включая RandomForestClassifier.

Результаты тестирования моделей представлены в таблице 1:

| Модель                     | Accuracy | Precision | Recall | F1-score |
|----------------------------|----------|-----------|--------|----------|
| Random Forest Classifier    | 0.74     | 0.81      | 0.81   | 0.81     |
| Decision Tree Classifier    | 0.71     | 0.80      | 0.69   | 0.74     |
| Blending ensemble           | 0.68     | 0.74      | 0.81   | 0.77     |

---

## Заключение
В результате работы были обучены и проанализированы различные модели. Лучшие результаты продемонстрировала модель RandomForestClassifier. Проект направлен на автоматизацию обработки медицинских изображений с использованием методов машинного обучения для извлечения количественной информации из диагностических изображений.

---

## Список литературы
1. B. Kocak, E.S. Durmaz, E. Ates, O. Kilickesmez. Radiomics with artificial intelligence: a practical guide for beginners. Affiliation: Department of Radiology Istanbul Training and Research Hospital, İstanbul, Turkey. 2019 Nov;25(6): 485–495.
2. M. E. Mayerhoefer, A. Materka, G. Langs, I. Häggström, P. Szczypiński, P. Gibbs, G. Cook. Introduction to Radiomics. Citation: Journal of Nuclear Medicine April 2020, 61(4): 488-495.
3. B. A. Varghese, S. Y. Cen, D. H. Hwang, V. A. Duddalwar. Texture Analysis of Imaging: What Radiologists Need to Know. Citation: American Journal of Roentgenology. 2019;212: 520-528.
4. C. Hassani, F. Saremi, B. A. Varghese, V. Duddalwar. Myocardial Radiomics in Cardiac MRI. Citation: American Journal of Roentgenology. 2020;214: 536-545.
