# 📱 Guía para Continuar el Proyecto desde Cualquier Lugar

## 🚀 Primera vez en un nuevo equipo

### 1. Clonar el repositorio
```bash
git clone https://github.com/MrSpain2104/cluster.git
cd cluster
```

### 2. Crear entorno virtual
```bash
# Windows (PowerShell)
python -m venv .venv
.\.venv\Scripts\Activate.ps1

# Linux/Mac
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Instalar dependencias
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Abrir Jupyter
```bash
jupyter lab
# o
jupyter notebook
```

---

## 🔄 Flujo de trabajo diario

### Antes de empezar (descargar cambios)
```bash
git pull origin main
```

### Durante el trabajo
```bash
# Ver archivos modificados
git status

# Agregar cambios específicos
git add CC_GENERAL_analysis.ipynb
git add CC_GENERAL_modelado.ipynb

# O agregar todos los cambios
git add .

# Hacer commit
git commit -m "Descripción de los cambios realizados"

# Ejemplo:
# git commit -m "Añadido análisis de outliers y nuevas visualizaciones"
# git commit -m "Optimizado número de clusters a 4"
# git commit -m "Agregadas estrategias de retención por segmento"
```

### Al terminar (subir cambios)
```bash
git push origin main
```

---

## 📋 Comandos útiles de Git

### Ver historial de cambios
```bash
git log --oneline
```

### Ver diferencias antes de commit
```bash
git diff
```

### Deshacer cambios no guardados
```bash
# Deshacer cambios en un archivo específico
git checkout -- nombre_archivo.ipynb

# Deshacer todos los cambios no guardados (¡cuidado!)
git reset --hard
```

### Crear una nueva rama para experimentar
```bash
# Crear y cambiar a nueva rama
git checkout -b feature/nueva-funcionalidad

# Trabajar normalmente y hacer commits
git add .
git commit -m "Experimentando con DBSCAN"

# Subir la nueva rama
git push -u origin feature/nueva-funcionalidad

# Volver a main
git checkout main
```

### Actualizar desde GitHub
```bash
# Descargar y fusionar cambios
git pull origin main

# Solo descargar (sin fusionar)
git fetch origin
```

---

## 🔧 Troubleshooting

### Error: "Please configure your identity"
```bash
git config user.name "MrSpain2104"
git config user.email "tu_email@example.com"
```

### Error: "Updates were rejected"
```bash
# Primero descargar cambios remotos
git pull origin main

# Si hay conflictos, resolverlos manualmente
# Luego hacer commit y push
git add .
git commit -m "Resolver conflictos"
git push origin main
```

### Conflictos en notebooks
Los notebooks de Jupyter pueden generar conflictos complicados. Opciones:

1. **Mantener tu versión**:
```bash
git checkout --ours archivo.ipynb
git add archivo.ipynb
```

2. **Mantener versión remota**:
```bash
git checkout --theirs archivo.ipynb
git add archivo.ipynb
```

3. **Usar extensión nbdime** (recomendado):
```bash
pip install nbdime
nbdime config-git --enable --global
```

---

## 📱 Workflow recomendado en la calle

### Opción 1: Desde laptop/tablet
1. `git pull` - Descargar última versión
2. Trabajar en los notebooks
3. `git add .` y `git commit -m "mensaje"`
4. `git push` - Subir cambios

### Opción 2: Desde GitHub web (ediciones rápidas)
1. Ir a https://github.com/MrSpain2104/cluster
2. Navegar al archivo
3. Click en ✏️ (Edit)
4. Hacer cambios
5. Scroll down → "Commit changes"

### Opción 3: GitHub Codespaces (ideal para mobile)
1. Ir a https://github.com/MrSpain2104/cluster
2. Click en "Code" → "Codespaces" → "New codespace"
3. Esperar que cargue el ambiente
4. Trabajar directamente en el navegador
5. Los cambios se sincronizan automáticamente

---

## 🌐 Recursos útiles

- **Repositorio**: https://github.com/MrSpain2104/cluster
- **Documentación Git**: https://git-scm.com/doc
- **GitHub Desktop** (GUI para Git): https://desktop.github.com/
- **VS Code** con extensión Git: Recomendado para manejar conflictos

---

## ✅ Checklist antes de hacer push

- [ ] El código funciona sin errores
- [ ] Los notebooks están ejecutados con outputs visibles
- [ ] No hay datos sensibles o contraseñas
- [ ] El README está actualizado (si es necesario)
- [ ] El commit tiene un mensaje descriptivo

---

## 🎯 Tips finales

1. **Commits frecuentes**: Mejor hacer commits pequeños y frecuentes que uno grande
2. **Mensajes claros**: Usa mensajes descriptivos: "Añadido análisis de correlación" vs "update"
3. **Pull antes de push**: Siempre haz `git pull` antes de `git push`
4. **Ramas para experimentos**: Si vas a hacer cambios grandes, usa una rama nueva
5. **Backups**: GitHub es tu backup, pero considera clonar también en otro lugar

---

**¡Listo para trabajar desde cualquier lugar! 🚀**
