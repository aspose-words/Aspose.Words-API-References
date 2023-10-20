---
title: Metered.SetMeteredKey
linktitle: SetMeteredKey
articleTitle: SetMeteredKey
second_title: Aspose.Words para .NET
description: Metered SetMeteredKey método. Establece la clave pública y privada medida. Si compra una licencia medida cuando inicie la aplicación se debe llamar a esta API normalmente esto es suficiente. Sin embargo si siempre no se pueden cargar los datos de consumo y excede las 24 horas la licencia se establecerá en estado de evaluación para evitar tal caso debe verificar periódicamente el estado de la licencia si está en estado de evaluación llame a esta API nuevamente en C#.
type: docs
weight: 20
url: /es/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Establece la clave pública y privada medida. Si compra una licencia medida, cuando inicie la aplicación, se debe llamar a esta API; normalmente, esto es suficiente. Sin embargo, si siempre no se pueden cargar los datos de consumo y excede las 24 horas, la licencia se establecerá en estado de evaluación, para evitar tal caso, debe verificar periódicamente el estado de la licencia; si está en estado de evaluación, llame a esta API nuevamente.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| publicKey | String | Llave pública |
| privateKey | String | llave privada |

## Ejemplos

Muestra cómo activar una licencia medida y realizar un seguimiento del crédito/consumo.

```csharp
// Cree una nueva licencia medida y luego imprima sus estadísticas de uso.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Opere usando Aspose.Words y luego imprima nuestras estadísticas medidas nuevamente para ver cuánto gastamos.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// El mecanismo de licencia medida de Aspose no envía los datos de uso al servidor de compra cada vez,
// necesitas usar la espera.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Ver también

* class [Metered](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
