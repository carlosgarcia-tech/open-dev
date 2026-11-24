# OpenDev-carlos

**Comunidad educativa de código abierto para aprender Java desde cero.**

OpenDev es un repositorio colaborativo donde estudiantes y personas que empiezan en la programación aprenden Java practicando, leyendo documentación clara y contribuyendo a un proyecto real. No es una colección de ejercicios sueltos: es una comunidad de aprendizaje con reglas de contribución, revisión de código y una ruta progresiva.

## Misión

Hacer que el desarrollo de software sea más accesible mediante un entorno de aprendizaje estructurado, colaborativo y abierto.

## Visión

Construir una comunidad donde las personas principiantes desarrollen habilidades de programación de forma progresiva, colaboren en proyectos de código abierto y se familiaricen con prácticas profesionales de desarrollo.

## Objetivos

- Enseñar Java desde cero, sin asumir experiencia previa.
- Practicar con ejercicios que se publicarán de forma progresiva.
- Aprender Git, GitHub y el flujo de Pull Requests.
- Fomentar el código limpio y las convenciones compartidas.
- Ofrecer revisiones de código constructivas.
- Mantener todo el material educativo accesible y abierto.

## ¿Quién puede participar?

Cualquier persona interesada en aprender o enseñar programación. No se requiere experiencia profesional. Puedes participar como:

- **Learner:** usas el material para aprender, aunque no contribuyas con código.
- **Contributor:** abres issues, mejoras documentación o envías Pull Requests.
- **Maintainer:** revisas contribuciones y ayudas a mantener el repositorio, cuando el Owner lo autorice.

## ¿Qué puedes aprender?

- Fundamentos de Java y de la programación.
- Tipos de datos, operadores, control de flujo, bucles y métodos.
- Arrays y cadenas.
- Pruebas automatizadas con JUnit 5.
- Git, GitHub, ramas, commits y Pull Requests.
- Revisión de código y trabajo colaborativo.
- Convenciones de estilo y buenas prácticas.

Los temas más avanzados se incorporarán cuando el alumnado haya completado los fundamentos. No se publica material adelantado.

## Ruta de aprendizaje

| Módulo | Tema                                    |
| ------ | --------------------------------------- |
| 00     | Introducción a la programación y a Java |
| 01     | Fundamentos de Java                     |
| 02     | Variables, tipos y entrada/salida       |
| 03     | Operadores                              |
| 04     | Control de flujo                        |
| 05     | Bucles                                  |
| 06     | Métodos                                 |
| 07     | Arrays y cadenas                        |

Consulta [`docs/learning-path/README.md`](docs/learning-path/README.md) para ver el orden recomendado y los objetivos de cada módulo.

Los ejercicios se publicarán uno a uno, a medida que avance el alumnado. Esta versión inicial no incluye ejercicios ni soluciones.

Cada alumno resuelve los ejercicios en su propio fork, dentro de `users/TU-USUARIO/`. El repositorio compartido solo contiene el currículo y las mejoras generales. Consulta [`exercises/README.md`](exercises/README.md).

## Estructura del repositorio

```text
open-dev/
├── .github/            Plantillas, workflows y configuración de GitHub
├── .mvn/               Configuración del Maven Wrapper
├── docs/               Guías, ruta de aprendizaje y gobernanza
├── exercises/          Reservado para ejercicios progresivos
├── projects/           Reservado para proyectos futuros
├── resources/          Libros, documentación y enlaces útiles
└── src/                Aplicación Java de ejemplo y sus tests
```

Cada directorio incluye un README con su propósito. La aplicación Java vive en `src/`.

## Requisitos

- Java 25 LTS.
- Git.
- Una cuenta de GitHub para contribuir.
- Terminal básica.

No necesitas Maven instalado: el repositorio incluye el Maven Wrapper (`mvnw`).

## Entorno recomendado

- **JDK 25 LTS**, obligatorio.
- **IntelliJ IDEA Community** o **Apache NetBeans**, recomendado.
- **Maven Wrapper**, incluido en el repositorio.

Consulta [`docs/getting-started/installation.md`](docs/getting-started/installation.md) para configurarlo todo paso a paso.

## Primeros pasos

1. Lee [`docs/getting-started/installation.md`](docs/getting-started/installation.md).
2. Instala el JDK 25 con [`docs/getting-started/java-setup.md`](docs/getting-started/java-setup.md).
3. Comprueba el Maven Wrapper con [`docs/getting-started/maven.md`](docs/getting-started/maven.md).
4. Configura tu IDE con [`docs/getting-started/ide-setup.md`](docs/getting-started/ide-setup.md).
5. Configura Git con [`docs/getting-started/git-setup.md`](docs/getting-started/git-setup.md).
6. Configura GitHub con [`docs/getting-started/github-setup.md`](docs/getting-started/github-setup.md).
7. Clona el repositorio y verifica el entorno:

```bash
git clone https://github.com/carlosgarcia-tech/open-dev.git
cd open-dev
./mvnw clean verify
```

8. Empieza por [`docs/learning-path/00-introduction.md`](docs/learning-path/00-introduction.md).

## Comandos disponibles

| Comando                   | Propósito                                     |
| ------------------------- | --------------------------------------------- |
| `./mvnw clean verify`     | Compila, ejecuta tests, Checkstyle y Spotless |
| `./mvnw test`             | Ejecuta solo los tests                        |
| `./mvnw checkstyle:check` | Ejecuta Checkstyle                            |
| `./mvnw spotless:check`   | Comprueba el formato Java                     |
| `./mvnw spotless:apply`   | Aplica el formato Java                        |
| `./mvnw package`          | Genera el JAR en `target/`                    |

En Windows, usa `.\mvnw.cmd` en lugar de `./mvnw`.

## Flujo de contribución

1. Busca o abre un issue.
2. Haz fork del repositorio y clona tu fork.
3. Crea una rama desde `main` con el prefijo adecuado.
4. Realiza el cambio y añade tests cuando corresponda.
5. Ejecuta `./mvnw clean verify`.
6. Haz commits con Conventional Commits.
7. Abre un Pull Request y responde a la revisión.

La guía completa está en [`CONTRIBUTING.md`](CONTRIBUTING.md).

## Modelo de ramas

OpenDev usa un GitHub Flow simplificado:

- `main` es la única rama permanente y siempre debe estar estable.
- Los cambios entran mediante Pull Requests.
- Las ramas de trabajo se crean desde `main` y usan prefijos como `feat/`, `fix/`, `docs/`, `refactor/`, `test/`, `chore/` o `hotfix/`.
- El método de merge preferido es **squash and merge**.

No existe una rama `develop`.

## Convención de commits

Formato: `<tipo>(<alcance>): <descripción>`

```text
docs(learning-path): add variables module
fix(fundamentals): correct integer division example
docs(installation): improve Java setup guide
```

Tipos permitidos: `feat`, `fix`, `docs`, `test`, `refactor`, `style`, `chore`, `build`, `ci`, `perf` y `revert`. La descripción empieza en minúscula, no termina en punto y no supera 72 caracteres.

## Pull Requests

Todo Pull Request debe describir qué cambia y por qué, indicar cómo se probó, pasar CI y recibir la aprobación de un maintainer. Usa la plantilla incluida y revisa [`docs/guides/pull-requests.md`](docs/guides/pull-requests.md).

## Comunidad

- Sigue el [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md).
- Consulta [`SUPPORT.md`](SUPPORT.md) para saber dónde pedir ayuda.
- Reporta vulnerabilidades de forma privada según [`SECURITY.md`](SECURITY.md).
- Las normas de convivencia y revisión están en [`docs/guides/code-review.md`](docs/guides/code-review.md).

## Roadmap

El plan por fases está en [`ROADMAP.md`](ROADMAP.md). El proyecto permanece en versión `0.x` hasta que la estructura educativa y el flujo de contribución sean estables.

## Licencia

OpenDev se distribuye bajo la licencia MIT. Consulta [`LICENSE`](LICENSE) y [`NOTICE`](NOTICE).

## Mantenimiento

Actualmente el repositorio es mantenido por el Owner del proyecto, que actúa como maintainer, technical lead y revisor principal. Los roles y el proceso de decisión se documentan en [`docs/governance/roles.md`](docs/governance/roles.md) y [`docs/governance/decision-making.md`](docs/governance/decision-making.md). La configuración pendiente de GitHub está en [`docs/governance/github-settings.md`](docs/governance/github-settings.md).
