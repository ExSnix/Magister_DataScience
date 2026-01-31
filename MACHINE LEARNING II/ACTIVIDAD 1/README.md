# Actividad 1 — Predicción de churn con Regresión Logística

**Contexto.** Una  empresa  de  telecomunicaciones  desea  predecir  qué  clientes  tienen  mayor  probabilidad  de fugarse(*churn*), para diseñar campañas de retención. Se cuenta con un dataset de clientes, sus características de uso y una  etiqueta  binaria  que  indica  si  el  cliente  se  fue  (churn  =  1)  o  se  mantuvo  (churn  =  0).El  objetivo  de  esta actividad es construir y evaluar modelos de regresión logística, comparando:

1. Un modelo con *features* “básicas” (preprocesadas).
2. Un modelo con *transformaciones polinomiales* sobre las featuresnuméricas.
3. Modelos con *penalización* (regularización) para controlar complejidad.

La evaluación debe realizarse mediante validación cruzada *k-fold*, utilizando *matriz de confusión*, curva *ROC* y curva *Precision–Recall*, en línea con lo visto en la clase.


## 🔎 Descripción de Variables — Dataset de Churn

El dataset contiene información demográfica, contractual y de uso de servicios de clientes de telecomunicaciones.  
La variable objetivo es **Churn**, que indica si el cliente se dio de baja del servicio.

---

### 📋 Diccionario de Variables

| Variable | Tipo | Descripción |
|----------|------|-------------|
| **customerID** | Identificador | Código único del cliente | 
| **gender** | Categórica binaria | Sexo del cliente | 
| **SeniorCitizen** | Binaria (0/1) | Indica si el cliente es adulto mayor |
| **Partner** | Binaria | Indica si tiene pareja |
| **Dependents** | Binaria | Si tiene dependientes |
| **tenure** | Numérica continua | Meses que lleva como cliente |
| **PhoneService** | Binaria | Servicio telefónico contratado |
| **MultipleLines** | Categórica | Si tiene múltiples líneas telefónicas |
| **InternetService** | Categórica | Tipo de internet (DSL, Fiber optic, None) |
| **OnlineSecurity** | Categórica | Servicio de seguridad online |
| **OnlineBackup** | Categórica | Servicio de respaldo en la nube |
| **DeviceProtection** | Categórica | Protección de dispositivos |
| **TechSupport** | Categórica | Soporte técnico contratado |
| **StreamingTV** | Categórica | Servicio de televisión en streaming |
| **StreamingMovies** | Categórica | Servicio de películas en streaming |
| **Contract** | Categórica | Tipo de contrato (mensual, anual, 2 años) |
| **PaperlessBilling** | Binaria | Facturación digital |
| **PaymentMethod** | Categórica | Método de pago |
| **MonthlyCharges** | Numérica | Cargo mensual del servicio |
| **TotalCharges** | Numérica | Total histórico pagado |
| **Churn** | Variable objetivo | YES = cliente se fue,NO = cliente se quedó |

