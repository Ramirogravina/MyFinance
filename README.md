# MyFinance
diff --git a/README.md b/README.md
index 4064402b60d583985ff373cfea02199fd7729dcf..bb8c5916757352d6bcf995a9108fe875981c6c27 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,166 @@
-# MyFinance
\ No newline at end of file
+# MyFinance Web App
+
+Simulador y tracker de portfolio financiero ficticio (mobile-first) pensado para uso personal.
+
+> **Stack esperado:** React + Vite + TypeScript + Tailwind (sin Next.js), deploy en Vercel y persistencia en `localStorage`.
+
+---
+
+## 🚀 Qué hace esta app
+
+- Simula la evolución de una cartera con:
+  - CEDEARs
+  - Bonos argentinos
+  - ETFs
+  - Acciones USA
+- Permite registrar **transacciones históricas** (compra ficticia).
+- Calcula automáticamente:
+  - Cantidad de shares/nominales
+  - Valor actual
+  - P/L absoluto
+  - Retorno %
+  - Allocation
+  - Rendimiento total
+- UI responsive estilo fintech (mobile-first, dark mode).
+
+---
+
+## 🧩 Funcionalidades principales
+
+### Portfolio / Holdings
+- Alta de transacción con:
+  - Ticker (con búsqueda/autocomplete)
+  - Tipo de activo
+  - Monto invertido
+  - Moneda (ARS/USD)
+  - Fecha de compra
+  - Precio de compra (opcional/manual)
+- Cálculo automático de cantidad:
+
+```txt
+shares = investedAmount / purchasePrice
+```
+
+- Edición de transacciones (Editar / Duplicar / Eliminar).
+
+### Dashboard
+- Total Invested
+- Current Value
+- Total P/L
+- Return %
+- Allocation (pie chart)
+- Tarjetas de performance
+- Switch ARS/USD con conversión (dólar MEP)
+
+### Persistencia
+- Guardado local con `localStorage`
+- Sin backend y sin base de datos
+
+---
+
+## 🛠️ Requisitos
+
+- Node.js 20+
+- npm 10+ (o pnpm/yarn)
+- Cuenta de GitHub
+- Cuenta de Vercel
+
+---
+
+## ▶️ Ejecución local
+
+1. Clonar repo
+
+```bash
+git clone https://github.com/TU_USUARIO/MyFinance.git
+cd MyFinance
+```
+
+2. Instalar dependencias
+
+```bash
+npm install
+```
+
+3. Levantar entorno de desarrollo
+
+```bash
+npm run dev
+```
+
+4. Abrir en navegador
+
+- Desktop: `http://localhost:5173`
+- Mobile: usar Safari iPhone con la URL de red local que te muestra Vite
+
+---
+
+## 🧪 Scripts útiles
+
+```bash
+npm run dev        # desarrollo
+npm run build      # build producción
+npm run preview    # preview local del build
+npm run lint       # lint
+```
+
+---
+
+## ☁️ Deploy en Vercel (solo GitHub + Vercel)
+
+1. Hacer push a GitHub.
+2. En Vercel: **Add New Project**.
+3. Importar este repo.
+4. Framework preset: **Vite** (o autodetect).
+5. Build command: `npm run build`
+6. Output directory: `dist`
+7. Deploy.
+
+Cada push a `main` dispara un redeploy automático.
+
+---
+
+## 📁 Estructura sugerida del proyecto
+
+```txt
+src/
+  app/
+  components/
+    common/
+    charts/
+    holdings/
+    transactions/
+  pages/
+    Dashboard/
+    Portfolio/
+    AssetDetail/
+    Analytics/
+  features/
+    portfolio/
+      calculations/
+      hooks/
+      services/
+      types/
+  data/
+  utils/
+  styles/
+```
+
+---
+
+## 🔒 Aclaraciones
+
+- Es una app de simulación personal.
+- No conecta brokers.
+- No ejecuta operaciones reales.
+- No incluye autenticación ni multiusuario.
+
+---
+
+## 📌 Próximos pasos recomendados
+
+- Integrar cotizaciones en vivo por proveedor de market data.
+- Integrar cotización MEP en tiempo real.
+- Agregar tests unitarios para cálculos de portfolio.
+- Exportar/importar transacciones (JSON/CSV).
+
