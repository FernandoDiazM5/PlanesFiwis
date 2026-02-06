# Volante FIWIS - Promoción Escolar con IA

Página web promocional con asesor virtual integrado usando Gemini AI.

## 🚀 Configuración e Instalación

### Paso 1: Obtener tu API Key de Google Gemini

1. Ve a [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Inicia sesión con tu cuenta de Google
3. Haz clic en **"Get API Key"** o **"Crear clave de API"**
4. Selecciona **"Create API key in new project"**
5. Copia la API Key generada (guárdala en un lugar seguro)

### Paso 2: Configurar restricciones de la API Key (IMPORTANTE)

Para evitar uso no autorizado:

1. Ve a [Google Cloud Console](https://console.cloud.google.com/apis/credentials)
2. Encuentra tu API Key y haz clic en **"Edit"** (ícono de lápiz)
3. En **"Application restrictions"**:
   - Selecciona **"HTTP referrers (web sites)"**
   - Agrega: `https://TU-USUARIO.github.io/*` (reemplaza TU-USUARIO)
   - Ejemplo: `https://juanperez.github.io/*`
4. En **"API restrictions"**:
   - Selecciona **"Restrict key"**
   - Busca y selecciona: **"Generative Language API"**
5. Haz clic en **"Save"**

### Paso 3: Configurar el Repositorio de GitHub

1. **Crea un nuevo repositorio** en GitHub
2. **Sube todos los archivos** de este proyecto al repositorio:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/TU-REPO.git
   git push -u origin main
   ```

### Paso 4: Configurar GitHub Secret

1. Ve a tu repositorio en GitHub
2. Haz clic en **"Settings"** (Configuración)
3. En el menú lateral, busca **"Secrets and variables"** → **"Actions"**
4. Haz clic en **"New repository secret"**
5. Configura:
   - **Name:** `GEMINI_API_KEY`
   - **Secret:** Pega tu API Key de Gemini
6. Haz clic en **"Add secret"**

### Paso 5: Habilitar GitHub Pages

1. En tu repositorio, ve a **"Settings"** → **"Pages"**
2. En **"Source"**, selecciona:
   - **Source:** GitHub Actions
3. ¡Listo! GitHub Actions se encargará del deploy automático

### Paso 6: Verificar el Deploy

1. Ve a la pestaña **"Actions"** en tu repositorio
2. Verás el workflow ejecutándose
3. Espera a que termine (aparecerá un ✅ verde)
4. Tu sitio estará disponible en: `https://TU-USUARIO.github.io/TU-REPO/`

## 🔧 Para desarrollo local

Si quieres probar localmente antes de subir:

1. Crea un archivo `config.js` en la raíz con:
   ```javascript
   window.GEMINI_API_KEY = 'TU_API_KEY_AQUI';
   ```

2. Abre `index.html` en tu navegador

**IMPORTANTE:** El archivo `config.js` está en `.gitignore` y NO se subirá a GitHub por seguridad.

## 📝 Notas de Seguridad

- ✅ La API Key NUNCA se expone en el código fuente
- ✅ La API Key se inyecta solo durante el deploy
- ✅ Configura restricciones de dominio en Google Cloud
- ✅ El archivo `config.js` está ignorado por Git

## 🛠️ Tecnologías Utilizadas

- HTML5 + TailwindCSS
- JavaScript Vanilla
- Google Gemini AI API
- GitHub Actions para CI/CD
- GitHub Pages para hosting

## 📞 Contacto

WhatsApp: 989 133 109 / 986 876 523

---

**Fiwis: Somos más conectados** 🚀
