---
title: Metered.SetMeteredKey
second_title: Referencia de API de Aspose.Words para .NET
description: Metered método. Establece la clave pública y privada medidas. Si compra una licencia medida cuando inicie la aplicación esta API debe llamarse normalmente esto es suficiente. Sin embargo si siempre falla al cargar los datos de consumo y excede las 24 horas la licencia se establecerá en estado de evaluación para evitar tal caso debe verificar regularmente el estado de la licencia si es estado de evaluación llame a esta API nuevamente.
type: docs
weight: 20
url: /es/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Establece la clave pública y privada medidas. Si compra una licencia medida, cuando inicie la aplicación, esta API debe llamarse, normalmente, esto es suficiente. Sin embargo, si siempre falla al cargar los datos de consumo y excede las 24 horas, la licencia se establecerá en estado de evaluación, para evitar tal caso, debe verificar regularmente el estado de la licencia, si es estado de evaluación, llame a esta API nuevamente.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| publicKey | String | Llave pública |
| privateKey | String | llave privada |

### Ejemplos

Muestra cómo activar una licencia medida y realizar un seguimiento del crédito/consumo.

```csharp
// Cree una nueva licencia medida y luego imprima sus estadísticas de uso.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Opera usando Aspose.Words, y luego imprime nuestras estadísticas medidas nuevamente para ver cuánto gastamos.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// El mecanismo de licencias medidas de Aspose no envía los datos de uso al servidor de compras cada vez,
// necesitas usar la espera.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Ver también

* class [Metered](../)
* espacio de nombres [Aspose.Words](../../metered/)
* asamblea [Aspose.Words](../../../)


