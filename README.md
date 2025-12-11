# Proyecto 3: RPTLS  
*Piedra, Papel, Tijera, Lagarto, Spock* — Implementado en **Ruby** con OOP, estrategias de IA y GUI en **Shoes**.

## Integrantes
- **Alejandra Mármol** – `2010408`  
- **Rosa Ramírez** – `2010527`

## Características Clave 

### Jerarquía de Jugadas
- Clase abstracta `Jugada`.
- 5 subclases: `Piedra`, `Papel`, `Tijera`, `Lagarto`, `Spock`.
- Método `puntos(contrincante)` → `[1,0]`, `[0,1]`, o `[0,0]`.
- Todas las **10 reglas** del juego implementadas.

### Jerarquía de Estrategias
- Clase base `Estrategia` con semilla global:  
  ```ruby
  @@semillaPadre = 42   # garantiza reproducibilidad

**5 estrategias:**
Manual, Uniforme, Sesgada, Copiar, Pensar

## Clase Partida
Modos: rondas(n) y alcanzar(n)
Historial completo de rondas y puntuaciones

## Interfaz Gráfica (Shoes)
Selección dinámica de estrategias y parámetros
Visualización de imágenes y marcador en tiempo real
Controles: Siguiente Ronda, Jugar Automático, Reiniciar

## Ejecución
Requisitos:
Ruby ≥ 2.5 (obligatorio)
Shoes ≥ 4.0 (solo para GUI)

   ## Archivos
   RPTLS.rb
   Piedra.png   Papel.png   Tijera.png   Lagarto.png   Spock.png  (opcionales, pero recomendados para mejorar la experiencia visual)

   ## Comandos
   ruby RPTLS.rb                # modo interactivo (pregunta consola/GUI)
   ruby RPTLS.rb -c             # consola
   ruby RPTLS.rb -s             # Shoes (si está instalado)

## Reglas Implementadas
Tijera corta a Papel
Papel tapa a Piedra
Piedra aplasta a Lagarto
Lagarto envenena a Spock
Spock rompe a Tijera
Tijera decapita a Lagarto
Lagarto devora a Papel
Papel desautoriza a Spock
Spock vaporiza a Piedra
Piedra aplasta a Tijera
**Todas verificadas mediante polimorfismo.**
