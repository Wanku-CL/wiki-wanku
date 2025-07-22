# Roadmap MVP — Épicas y Cubicación Preliminar (Ago–Nov 2025)

## 1. Suposiciones de Capacidad
- **Periodo:** 04-ago-2025 al 21-nov-2025 (~16 semanas efectivas).
- **Equipo:** 5 FTE promedio.
  - **Web/BE/QA/BA:** Fernanda, Rodrigo, Maximiliano (3 personas multitarea).
  - **Mobile & MS OMR:** Paolo, Nicolás (2 personas).
  - **TL & Arq (parciales):** Carlos (TL), Carlos T (Arq).
- **Medida:** 1 **PW** = 1 persona trabajando 1 semana.
- Rango de error estimado: ±20% (velocidad aún desconocida).

### Escala de tamaños
| Tamaño | Rango PW | Ejemplos |
|--------|----------|----------|
| XS     | ≤ 2      | Guías puntuales, documentos pequeños |
| S      | 2–4      | Plan de pruebas, manuales de uso |
| M      | 5–8      | Diseño funcional/técnico sólido |
| L      | 9–14     | Desarrollo de un producto (web/mobile) MVP |
| XL     | 15–22    | Backend core + integración + seguridad |

---

## 2. Épicas y Cubicación

| Épica | Objetivo MVP (DoD resumido) | Streams principales | Tamaño | Rango PW | Dependencias clave | Riesgo |
|-------|-----------------------------|---------------------|--------|----------|---------------------|--------|
| **Requerimientos** | Casos de Uso completos (actor, flujo, reglas, C.A.), matriz de RNF | BA/Func (F/R/M) | M | 6–8 | Discovery cerrado, disponibilidad PO | Medio |
| **Diseño Funcional** | BPMN/Estados/Flujos + prototipos UI (lo/hi-fi) clave | BA + Web/Mobile | M | 5–7 | Reqs base, decisiones UX | Medio |
| **Diseño Técnico** | C4 (niveles 1–3), ERD v1, OpenAPI v1, lineamientos DevOps | Arq & DevOps (TL/C.T), Web/BE | M–L | 7–10 | Diseño funcional v1 | Alto |
| **Plan de Pruebas** | Estrategia QA, matriz de casos, tipos de prueba, criterios de salida | QA (F/R/M) | S | 2–4 | Reqs & Diseño Funcional | Bajo |
| **Desarrollo Backend** | APIs core (auth, evaluaciones, usuarios), lógica corrección, persistencia | Web/BE (F/R/M) | XL | 16–22 | Diseño técnico, ERD, OpenAPI | Alto |
| **Desarrollo Web** | UI core flujo principal (crear/gestionar eval.), consumo APIs, auth | Web/BE (F/R/M) | L | 10–14 | Backend mocks, diseño funcional | Medio |
| **Desarrollo Mobile** | App de captura/envío (login, cámara, sync), consumo APIs | Mobile (P/N) | L | 9–13 | Diseño funcional, contratos API | Medio |
| **Desarrollo MS OMR** | Servicio procesamiento imágenes (accuracy aceptable), API integrada | Mobile/OMR (P/N) + BE | L | 9–12 | Dataset/formato hojas, libs CV | Alto |
| **Testing (Ejecución)** | Pruebas unit/integración/contrato/E2E ejecutadas y reportadas; fixes críticos | QA + Todos | M | 6–8 | Plan de pruebas, features dev | Medio |
| **Documentación de Uso** | Manual usuario/admin + runbooks operativos MVP | BA + TL/Arq | S | 2–3 | Producto estable | Bajo |

**Total estimado:** **~72–101 PW** (encaja con ~80 PW disponibles aprox.).

---

## 3. Notas Clave
- **Paralelización:** Todas las áreas trabajan cada sprint (dual-track: BA refinando mientras devs construyen vertical slices).
- **Hitos de sincronización sugeridos:**
  - Fin S2: Contratos API + ERD v1 “congelados”.
  - Fin S3: Primer slice integrado (web/mobile/back) con mocks.
  - Fin S5: MS OMR v1 funcional integrado.
  - Fin S7: Flujo E2E probado (UAT interno).
- **Riesgos principales:** precisión del OMR, definición de RNF críticos, dependencia de PO para priorizar.

---

## 4. Distribución temporal sugerida (sin actividades)
* Ago (S1–S2): Requerimientos (M), Diseño Funcional (M), Diseño Técnico (parte), arranque Dev Backend/Web/Mobile/OMR con contratos mock (trabajo paralelo).
* Sep (S3–S4): Desarrollo BE/Web/Mobile/OMR avanza fuerte (L/XL), Plan de Pruebas (S) finalizado.
* Oct (S5–S6): Consolidar features, integrar OMR, afinar Backend; Testing ejecución (M) empieza en serio.
* Nov (S7–S8): Testing cierre, fixes, Documentación de Uso (S), hardening y salida MVP.

### Gantt Preliminar (Ago–Nov 2025) — Épicas MVP

**Leyenda:**  
**█** foco principal · **░** soporte/ajustes · **·** sin trabajo relevante  
**⚑** semana con capacidad reducida (Fiestas Patrias CL: 17–21 sep)

| Épica / Semana | W1<br>(04–08 ago) | W2<br>(11–15 ago) | W3<br>(18–22 ago) | W4<br>(25–29 ago) | W5<br>(01–05 sep) | W6<br>(08–12 sep) | W7⚑<br>(15–19 sep) | W8<br>(22–26 sep) | W9<br>(29 sep–03 oct) | W10<br>(06–10 oct) | W11<br>(13–17 oct) | W12<br>(20–24 oct) | W13<br>(27–31 oct) | W14<br>(03–07 nov) | W15<br>(10–14 nov) | W16<br>(17–21 nov) |
|----------------|:-----------------:|:-----------------:|:-----------------:|:-----------------:|:-----------------:|:-----------------:|:------------------:|:-----------------:|:----------------------:|:-------------------:|:-------------------:|:-------------------:|:-------------------:|:-------------------:|:-------------------:|:-------------------:|
| **Requerimientos**        | █ | █ | █ | ░ | ░ | · | · | · | · | · | · | · | · | · | · | · |
| **Diseño Funcional**      | █ | █ | █ | ░ | ░ | · | · | · | · | · | · | · | · | · | · | · |
| **Diseño Técnico**        | █ | █ | █ | ░ | ░ | · | · | · | · | · | · | · | · | · | · | · |
| **Plan de Pruebas**       | · | · | █ | █ | █ | · | · | · | · | · | · | · | · | · | · | · |
| **Desarrollo Backend**    | ░ | ░ | █ | █ | █ | █ | █ | █ | █ | █ | █ | ░ | ░ | ░ | · | · |
| **Desarrollo Web**        | ░ | ░ | ░ | █ | █ | █ | █ | █ | █ | █ | █ | █ | ░ | ░ | · | · |
| **Desarrollo Mobile**     | █ | █ | █ | █ | █ | █ | █ | █ | █ | █ | ░ | ░ | · | · | · | · |
| **Desarrollo MS OMR**     | █ | █ | █ | █ | █ | █ | █ | █ | █ | █ | ░ | ░ | · | · | · | · |
| **Testing (Ejecución)**   | · | · | · | · | ░ | ░ | ░ | ░ | █ | █ | █ | █ | █ | █ | · | · |
| **Documentación de Uso**  | · | · | · | · | · | · | · | · | · | · | · | · | █ | █ | █ | █ |

> Ajusta fácilmente los símbolos si cambian prioridades o capacidades.

> Nota: Semana del **17–21 de septiembre** con capacidad reducida (Fiestas Patrias CL).

---

## 5. Próximos Pasos
1. Validar rangos PW con el equipo (ajustar según disponibilidad real).
2. Confirmar criterios de éxito/accuracy del OMR.
3. Acordar alcance exacto del MVP (qué queda dentro/fuera en Web/Mobile).
4. Definir RNF críticos (seguridad, performance, offline).
5. Decidir nivel de automatización QA y herramientas.
