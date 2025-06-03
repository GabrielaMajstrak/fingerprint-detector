# Rozpoznawanie odcisków palców - szkieletyzacja i detekcja minucji

## 📋 Opis projektu

System do analizy odcisków palców oparty na szkieletyzacji obrazu oraz detekcji charakterystycznych punktów (minucji). Projekt implementuje dwa zaawansowane algorytmy szkieletyzacji oraz system wykrywania różnych typów minucji w odciskach palców.

**Autorzy:** Gabriela Majstrak, Jan Opala  
**Data:** Maj 2025

## 🎯 Cele projektu

- Implementacja i porównanie algorytmów szkieletyzacji (morfologiczna vs K3M)
- Detekcja i klasyfikacja minucji (zakończenia i bifurkacje)
- Analiza jakości różnych metod przetwarzania odcisków palców
- Filtrowanie artefaktów i poprawa jakości wykrywania

## 🚀 Główne funkcjonalności

### Algorytmy szkieletyzacji
- **Szkieletyzacja morfologiczna** - klasyczny algorytm oparty na operacjach erozji i otwarcia
- **Algorytm K3M** - zaawansowana czterofazowa metoda iteracyjnego usuwania pikseli

### Detekcja minucji
- Wykrywanie **zakończeń** (endpoints) - punkty gdzie linia papilarna kończy się
- Wykrywanie **bifurkacji** (bifurcations) - punkty rozgałęzienia linii
- Klasyfikacja na podstawie **crossing number**
- Zaawansowane filtrowanie fałszywych pozytywów

### Przetwarzanie obrazu
- Binaryzacja metodą Otsu z parametrem delta
- Binaryzacja adaptacyjna
- Operacje morfologiczne (erozja, dylatacja, otwarcie, zamknięcie)
- Detekcja granic odcisku na podstawie wariancji lokalnej

## 🛠️ Wymagania techniczne

### Biblioteki Python
```python
numpy          # Operacje na macierzach i pikselach
PIL            # Otwieranie i przetwarzanie obrazów
matplotlib     # Wizualizacja wyników
opencv-python  # Zaawansowane operacje na obrazach
scipy          # Operacje morfologiczne (opcjonalnie)
