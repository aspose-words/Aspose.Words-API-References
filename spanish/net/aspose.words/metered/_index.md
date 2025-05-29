---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words para .NET
description: ¡Desbloquea el poder de la clase Aspose.Words.Metered! Gestiona fácilmente tu clave medida con métodos eficientes para un procesamiento de documentos fluido.
type: docs
weight: 4850
url: /es/net/aspose.words/metered/
---
## Metered class

Proporciona métodos para establecer una clave medida.

```csharp
public class Metered
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Metered](metered/)() | Inicializa una nueva instancia de esta clase. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetProductName](../../aspose.words/metered/getproductname/)() | Devuelve el nombre del producto |
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | Establece claves públicas y privadas medidas. Si compra una licencia medida, al iniciar la aplicación, se debe llamar a esta API; normalmente, esto es suficiente. Sin embargo, si siempre no se pueden cargar los datos de consumo y exceden las 24 horas, la licencia se establecerá en estado de evaluación. Para evitar tal caso, debe verificar regularmente el estado de la licencia; si está en estado de evaluación, vuelva a llamar a esta API. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Obtiene crédito de consumo |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Obtiene el tamaño del archivo de consumo |
| static [IsMeteredLicensed](../../aspose.words/metered/ismeteredlicensed/)() | Verificar si el medidor tiene licencia |

## Ejemplos

En este ejemplo, se intentará establecer una clave pública y privada medida

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

Muestra cómo activar una licencia medida y realizar un seguimiento del crédito/consumo.

```csharp
// Cree una nueva licencia medida y luego imprima sus estadísticas de uso.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Is metered license accepted: {Metered.IsMeteredLicensed()}");
Console.WriteLine($"Product name: {metered.GetProductName()}");
Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Opere utilizando Aspose.Words y luego imprima nuevamente nuestras estadísticas medidas para ver cuánto gastamos.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// El mecanismo de licencias medidas de Aspose no envía los datos de uso al servidor de compra cada vez,
// necesitas usar espera.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
