# BRÚJULA Finanzas

PWA financiera personal, privada y mobile-first.

## Publicación en GitHub Pages

1. Sube estos archivos a la raíz del repositorio `brujula`:
   - `index.html`
   - `firestore.rules`
   - `README.md`
2. En GitHub, entra al repositorio.
3. Ve a **Settings > Pages**.
4. En **Build and deployment**, selecciona:
   - Source: **Deploy from a branch**
   - Branch: **main**
   - Folder: **/ root**
5. Guarda.
6. La URL debería quedar como:
   `https://diegomorissalazar-a11y.github.io/brujula/`

## Firebase

El archivo `index.html` ya viene con el proyecto Firebase configurado:

- Proyecto: `brujula-be291`
- Auth domain: `brujula-be291.firebaseapp.com`

En Firebase debes activar:

1. **Authentication > Sign-in method**
   - Email/Password
   - Google opcional

2. **Authentication > Settings > Authorized domains**
   - Agregar: `diegomorissalazar-a11y.github.io`

3. **Firestore Database**
   - Crear base de datos en modo producción.
   - Publicar las reglas incluidas en `firestore.rules`.

## Datos

La app funciona primero en localStorage y luego sincroniza con Firestore si el usuario inicia sesión.

Colecciones usadas:

- `users/{uid}/accounts`
- `users/{uid}/categories`
- `users/{uid}/movements`
- `users/{uid}/debts`
- `users/{uid}/savingsAccounts`

