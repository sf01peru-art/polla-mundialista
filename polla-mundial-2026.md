# Polla Mundialista 2026 ⚽
**USA · México · Canadá**

---

## 1. Objetivo

Página web para gestionar la Polla Mundialista 2026. Cada participante elabora **una lista fija** con las 48 selecciones ordenadas de mejor a peor. Con los resultados reales de cada partido se acumulan puntos automáticamente. Al final del torneo se reparten tres premios.

---

## 2. Participantes

- **Jugadores:** crean su lista y consultan la tabla de posiciones
- **Administrador:** ingresa los resultados de los partidos

> ¿Cuántos participantes esperan?

---

## 3. Flujo General

```
Jugador entra a la página
    → Ingresa nombre + email
    → Ordena las 48 selecciones de mejor (1°) a peor (48°)
    → Guarda su lista (no puede modificarla después)

Admin entra con contraseña (1234polla)
    → Ingresa el resultado de cada partido (ganador o empate)
    → Los puntajes de todos se recalculan automáticamente
    → Puede exportar / importar los datos (backup)

Todos ven la tabla de posiciones actualizada
```

---

## 4. La Lista de Selecciones

Cada participante ordena las **48 selecciones del Mundial 2026** usando listas desplegables (no escritura libre). Los equipos ya elegidos se deshabilitan para evitar duplicados.

- Puesto 1° → **48 puntos**
- Puesto 2° → **47 puntos**
- …
- Puesto 48° → **1 punto**

### Ejemplo

| Posición | Selección | Valor |
|:--------:|-----------|:-----:|
| 1° | Argentina | 48 pts |
| 2° | Francia | 47 pts |
| 3° | Brasil | 46 pts |
| … | … | … |
| 47° | Nueva Zelanda | 2 pts |
| 48° | Bolivia | 1 pt |

---

## 5. Sistema de Puntos

Los puntos se asignan en **todos los partidos del torneo** (104 en total: fase de grupos + eliminatorias).

### 5.1 Partido con ganador

El equipo ganador acumula sus puntos de lista para ese participante.

> Ana puso a Argentina 1° (48 pts) y a México 10° (39 pts).
> Argentina gana → Ana suma **48 pts**.

### 5.2 Partido empatado

Cada equipo aporta la **mitad** de sus puntos. Se aceptan decimales.

> Argentina empata con México:
> 48/2 + 39/2 = 24 + 19.5 = **43.5 pts**

### 5.3 Total del participante

```
Puntaje total = suma de puntos en todos los partidos del torneo
```

---

## 6. Premios y Desempates

### 6.1 Distribución de premios

| Lugar | Premio |
|:-----:|--------|
| 1° | 70% del pozo |
| 2° | 20% del pozo |
| 3° | 10% del pozo |

### 6.2 Reglas de empate en puntaje final

| Situación | Resultado |
|-----------|-----------|
| **Empate en 1°** (2 personas) | Comparten 70%+20% = 45% cada uno. **No hay 3° lugar.** |
| **Empate en 1°** (3 personas) | Comparten 70%+20%+10% = 33.3% cada uno. Premios agotados. |
| **Empate en 2°** (2 personas) | Comparten 20%+10% = 15% cada uno. **No hay 3° lugar.** |
| **Empate simultáneo en 1° y 2°** | Se reparte el 100% del pozo en partes iguales entre todos los empatados. |

#### Ejemplo empate simultáneo

> Carlos y Luisa empatan en 1° (misma puntuación).
> Pedro y Marta empatan en lo que sería el 2° (misma puntuación entre ellos).
> → Los 4 reciben **25% cada uno** (100% ÷ 4).

---

## 7. Estructura de la Página

| Sección | Descripción |
|---------|-------------|
| **Mi Lista** | Formulario con 48 desplegables para ordenar las selecciones |
| **Tabla** | Clasificación con puntaje acumulado y premios proyectados |
| **Partidos** | Calendario y resultados por fase |
| **Admin** | Ingresar resultados · exportar / importar datos |

---

## 8. Las 48 Selecciones

Lista de clasificados al Mundial 2026 (verificar con lista oficial FIFA antes de publicar).

### CONMEBOL — 6 cupos
| # | Selección |
|---|-----------|
| 1 | Argentina |
| 2 | Brasil |
| 3 | Colombia |
| 4 | Uruguay |
| 5 | Ecuador |
| 6 | Venezuela |

### CONCACAF — 6 cupos (incluye 3 sedes)
| # | Selección |
|---|-----------|
| 7 | Estados Unidos *(sede)* |
| 8 | Canadá *(sede)* |
| 9 | México *(sede)* |
| 10 | Panamá |
| 11 | Costa Rica |
| 12 | Honduras |

### UEFA — 16 cupos
| # | Selección |
|---|-----------|
| 13 | España |
| 14 | Francia |
| 15 | Inglaterra |
| 16 | Alemania |
| 17 | Portugal |
| 18 | Países Bajos |
| 19 | Bélgica |
| 20 | Italia |
| 21 | Suiza |
| 22 | Croacia |
| 23 | Dinamarca |
| 24 | Austria |
| 25 | Escocia |
| 26 | Serbia |
| 27 | Turquía |
| 28 | Hungría |

### CAF — 9 cupos
| # | Selección |
|---|-----------|
| 29 | Marruecos |
| 30 | Senegal |
| 31 | Egipto |
| 32 | Nigeria |
| 33 | Camerún |
| 34 | Sudáfrica |
| 35 | Ghana |
| 36 | Mali |
| 37 | Argelia |

### AFC — 8 cupos
| # | Selección |
|---|-----------|
| 38 | Japón |
| 39 | Corea del Sur |
| 40 | Irán |
| 41 | Australia |
| 42 | Arabia Saudita |
| 43 | Iraq |
| 44 | Jordania |
| 45 | Uzbekistán |

### OFC — 1 cupo
| # | Selección |
|---|-----------|
| 46 | Nueva Zelanda |

### Repechaje intercontinental — 2 cupos
| # | Selección |
|---|-----------|
| 47 | *(por confirmar)* |
| 48 | *(por confirmar)* |

> ⚠️ Algunos equipos de UEFA y CAF están pendientes de confirmación oficial. Ajustar antes de publicar.

---

## 9. Exportar / Importar Datos

El admin podrá desde el panel:

- **Exportar:** descarga un archivo `.json` con todos los datos (listas, resultados, puntajes)
- **Importar:** carga un archivo `.json` previamente exportado para restaurar el estado

Esto protege los datos si se borra el caché o se cambia de computador.

---

## 10. Configuración Confirmada

| Parámetro | Valor |
|-----------|-------|
| Nombre | Polla Mundialista |
| Selecciones | 48 equipos |
| Puntos por lista | 1 pt (48°) → 48 pts (1°) |
| Empates | Divide puntos en dos · acepta decimales |
| Ingreso de lista | Listas desplegables estandarizadas |
| Partidos | 104 en total (grupos + eliminatorias) |
| Premios | 70% / 20% / 10% |
| Alojamiento | Local (localStorage) |
| Contraseña admin | `1234polla` |
| Backup | Exportar / importar JSON |

---

## 11. Pendientes

- [ ] Confirmar los 2 clasificados del repechaje intercontinental
- [ ] Verificar lista completa UEFA y CAF con clasificados oficiales
- [ ] Confirmar cantidad de participantes esperados
