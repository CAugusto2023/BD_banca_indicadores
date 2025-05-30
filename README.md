# BD_banca_indicadores
🏦 Caso Propuesto: Gestión de Indicadores Diarios en el Banco FinanExpress Contexto: El Banco FinanExpress necesita implementar un sistema para registrar, analizar y reportar indicadores bancarios diarios que permitan a los gerentes de distintas áreas monitorear el desempeño operativo y financiero de la institución en tiempo real.

🎯 Objetivos del sistema: Registrar indicadores diarios por sucursal.

Controlar el origen del dato (sistema fuente que reporta el indicador).
Almacenar los valores reales y los valores objetivo (meta) de cada indicador.
Permitir consultas históricas y comparaciones por día, semana, mes y sucursal.
Detectar desviaciones entre valores reales y metas.
Permitir la clasificación de indicadores por categoría (ej: liquidez, riesgo, atención al cliente, cumplimiento normativo, etc.).

Sucursal

-ID
  
-Nombre
  
-Ciudad
  
-Región

Indicador

-ID

-Nombre

-Descripción

-Unidad de medida

-Categoría (Ej. “Riesgo de crédito”, “Liquidez”, “Atención al cliente”)

SistemaFuente

-ID

-Nombre del sistema

-Responsable

RegistroIndicadorDiario

-ID

-Fecha

-IDIndicador

-IDSucursal

-ValorReal

-ValorMeta

-IDSistemaFuente

DesviacionIndicador (opcional, derivada o materializada)

-IDRegistroIndicadorDiario

-DiferenciaAbsoluta

-DiferenciaPorcentual

-Clasificación (Ej. Sin desvío, Ligera, Crítica)

📘 Reglas de negocio: Cada indicador debe estar asociado a una categoría.

Una sucursal debe reportar sus indicadores diariamente antes de las 10:00 a.m.
El sistema debe permitir identificar qué sistema fuente proporcionó cada dato.
Si el valor real difiere más del 10% de la meta, debe marcarse como “Crítica”.

💡 Ejemplos de Indicadores: Monto total desembolsado (en soles/dólares).

Número de nuevas cuentas abiertas.
Promedio de tiempo de atención al cliente (minutos).
Ratio de morosidad (%).
Cantidad de operaciones realizadas por canal digital.

🛠️ Posibles consultas: ¿Cuál fue la desviación diaria del indicador "Monto desembolsado" en todas las sucursales la última semana?

¿Qué indicadores de la categoría "Riesgo de crédito" han tenido desvíos críticos este mes?
¿Qué sistema fuente ha reportado más inconsistencias en los últimos 30 días?
¿Cómo evolucionó el indicador "Número de cuentas abiertas" en Lima durante el último trimestre?

Diagra entidad relación
https://private-user-images.githubusercontent.com/30308669/443466999-0fe023d5-69ca-4631-a745-19e503f5bf46.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NDg1Nzk3ODYsIm5iZiI6MTc0ODU3OTQ4NiwicGF0aCI6Ii8zMDMwODY2OS80NDM0NjY5OTktMGZlMDIzZDUtNjljYS00NjMxLWE3NDUtMTllNTAzZjViZjQ2LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNTA1MzAlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjUwNTMwVDA0MzEyNlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTliZDk3MjRlOTg0MDI1YTA4MmNkYzQ1YzBjOTVlODhkOWNmYzIyYTM0MjBjNGY2OGM1MzBjN2I5ZTgyMjQyYTUmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0In0.oMCpp3shyS5Gr7iQrfvsNlt1UVFERdiAtd8K2r5mCN0


Diseño lógico
bd_banca_indicadores_diarios_1

Modelo Físico
image
