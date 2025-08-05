# 🧓 Análisis de Datos en una Residencia de Mayores

Este proyecto simula un entorno real de gestión en una residencia geriátrica. A partir de datos ficticios pero **realistas** (2022–2025), analizo patrones de ingreso, estancias y motivos clínicos para proponer acciones de **marketing y gestión**.

---

## 🎯 Objetivo

- Detectar **estacionalidad** en los motivos de ingreso.
- Comparar **duración media** por motivo de ingreso.
- Identificar **perfiles de larga estancia**.
- Sugerir **acciones de marketing** basadas en datos.

---

## 🔍 Hipótesis

1. En **agosto** aumentan ingresos por “**Vacaciones para la familia**”.
2. En **julio, agosto, diciembre y enero** casi no hay **prótesis** por vacaciones médicas.
3. Ingresos por **demencia** o **mayor dependencia** → **estancias indefinidas**.
4. Entre >85 años, proporción **mujeres:hombres ≈ 5:1** (mayor esperanza de vida).
5. **Marzo y abril** tienen picos por **campaña publicitaria**.
6. **Prótesis de cadera/rodilla** → **mayor y más rápida recuperación**.

---

## 🧾 Datos

- **Fuente**: simulación propia coherente con las hipótesis.
- **Archivo**: `datos_residencia_hipotesis_1000.xlsx` (1.000 registros, 2022–2025).

### Diccionario de datos (principales columnas)

| Columna           | Descripción                                                     | Ejemplo                 |
|-------------------|-----------------------------------------------------------------|-------------------------|
| `Paciente_ID`     | Identificador simulado del paciente                             | `P0123`                 |
| `Fecha_ingreso`   | Fecha de ingreso                                                | `2024-03-15`            |
| `Fecha_salida`    | Fecha de salida (puede ser nula si sigue ingresado)            | `2024-04-10` / `NaN`    |
| `Edad`            | Edad en años                                                    | `82`                    |
| `Sexo`            | `M`/`F`                                                         | `F`                     |
| `Motivo_ingreso`  | Motivo principal (p. ej., Demencia, Vacaciones…)               | `Vacaciones para la familia` |
| `%_Mejoría`       | % de mejoría clínica (no aplica en vacaciones/demencia)        | `78.5`                  |
| `Alta`            | `Sí`/`No`                                                       | `Sí`                    |
| `Exitus`          | Fallecimiento (`Sí`/`No`)                                       | `No`                    |
| `Mes`*            | Mes numérico derivado de `Fecha_ingreso`                        | `8`                     |
| `Tiempo_ingreso`* | Estancia en días (`Fecha_salida - Fecha_ingreso`)               | `34`                    |

\* Columnas derivadas en el análisis.

---

## 🛠️ Herramientas

- **Python**: `pandas`, `matplotlib`, `seaborn` (y/o `plotly`)
- EDA, agrupaciones, estadísticas descriptivas y visualización.

---

## 📈 Visualizaciones clave

**1) Duración media por motivo de ingreso**  
Muestra estancias cortas en “Vacaciones…”, largas/indefinidas en Demencia/Dependencia.
  
<img width="985" height="584" alt="grafico1" src="https://github.com/user-attachments/assets/48500e35-e509-4594-8130-6036316bbb38" />


**2) Ingresos por mes y motivo**  
Estacionalidad clara en **agosto** (Vacaciones) y picos en **marzo/abril** (campaña).
  

<img width="1380" height="684" alt="grafico2" src="https://github.com/user-attachments/assets/359ef0b2-e285-435a-81ca-5001da5ef6dc" />

---

## 🧠 Hallazgos y propuestas

- **Demencia** y **Mayor dependencia** → pacientes sin fecha de salida → **ingresos estables**.
- **Vacaciones (agosto)** → **alto volumen** con estancias cortas → campañas estacionales.
- **Prótesis** → **alta recuperación** → campañas quirúrgicas fuera de meses de vacaciones médicas.
- **Recomendación**: segmentar campañas por **mes/motivo**, ajustar recursos a picos.

---



## ✍️ Autor

**Alberto Saavedra**  
[LinkedIn](www.linkedin.com/in/alberto-saavedra-aguilar-303274134) 

