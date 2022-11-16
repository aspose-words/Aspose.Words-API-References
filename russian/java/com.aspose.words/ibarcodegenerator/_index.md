---
title: IBarcodeGenerator
second_title: Справочник по API Aspose.Words для Java
description: Публичный интерфейс для пользовательского генератора штрих-кода.
type: docs
weight: 632
url: /ru/java/com.aspose.words/ibarcodegenerator/
---
```
public interface IBarcodeGenerator
```

 Публичный интерфейс для пользовательского генератора штрих-кода. Реализация должна быть предоставлена пользователем. Экземпляр генератора должен быть передан через[FieldOptions.getBarcodeGenerator()](../../com.aspose.words/fieldoptions\#getBarcodeGenerator--) / [FieldOptions.setBarcodeGenerator(com.aspose.words.IBarcodeGenerator)](../../com.aspose.words/fieldoptions\#setBarcodeGenerator-com.aspose.words.IBarcodeGenerator-) имущество.
## Методы

| Метод | Описание |
| --- | --- |
| [getBarcodeImage(BarcodeParameters parameters)](#getBarcodeImage-com.aspose.words.BarcodeParameters-) | Сгенерировать изображение штрих-кода, используя набор параметров (для поля DisplayBarcode). |
| [getOldBarcodeImage(BarcodeParameters parameters)](#getOldBarcodeImage-com.aspose.words.BarcodeParameters-) | Сгенерируйте изображение штрих-кода, используя набор параметров (для устаревшего поля штрих-кода). |
### getBarcodeImage(BarcodeParameters parameters) {#getBarcodeImage-com.aspose.words.BarcodeParameters-}
```
public abstract BufferedImage getBarcodeImage(BarcodeParameters parameters)
```


Сгенерировать изображение штрих-кода, используя набор параметров (для поля DisplayBarcode).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| parameters | [BarcodeParameters](../../com.aspose.words/barcodeparameters) | Набор параметров |

**Возвращает:**
java.awt.image.BufferedImage — изображение, представляющее сгенерированный штрих-код.
### getOldBarcodeImage(BarcodeParameters parameters) {#getOldBarcodeImage-com.aspose.words.BarcodeParameters-}
```
public abstract BufferedImage getOldBarcodeImage(BarcodeParameters parameters)
```


Сгенерируйте изображение штрих-кода, используя набор параметров (для устаревшего поля штрих-кода).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| parameters | [BarcodeParameters](../../com.aspose.words/barcodeparameters) | Набор параметров |

**Возвращает:**
java.awt.image.BufferedImage — изображение, представляющее сгенерированный штрих-код.