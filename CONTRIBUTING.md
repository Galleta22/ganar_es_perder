# Flujo de trabajo - Git Flow Simplificado

## Ramas principales

### `main`
- Contiene el código estable y funcional del proyecto.
- Solo se actualiza mediante merges aprobados desde `develop`.
- Nadie hace commits directos aquí.

### `develop`
- Rama de integración y desarrollo activo.
- Todas las features se mergean aquí antes de pasar a `main`.
- Es la rama base para crear nuevas ramas `feature/`.

---

## Ramas de trabajo

### `feature/<nombre>`
- Se crea a partir de `develop`.
- Cada integrante trabaja su funcionalidad en su propia rama.
- Al terminar, se hace un Pull Request hacia `develop`.

**Ejemplos:**
- `feature/blackjack`
- `feature/tragamonedas`
- `feature/menu-principal`
- `feature/poderes`

---

## Flujo paso a paso

```bash
# 1. Asegurarse de estar en develop actualizado
git checkout develop
git pull origin develop

# 2. Crear rama para la nueva funcionalidad
git checkout -b feature/nombre-funcionalidad

# 3. Trabajar, hacer commits...
git add .
git commit -m "Descripción del cambio"

# 4. Subir la rama
git push origin feature/nombre-funcionalidad

# 5. Crear Pull Request en GitHub: feature/... -> develop

# 6. Una vez aprobado, merge a develop
# 7. Cuando develop esté estable, merge a main
```

---

## Reglas del equipo
- No hacer push directo a `main`.
- Los merges a `develop` requieren al menos una revisión.
- Nombrar los commits de forma clara y en español.
