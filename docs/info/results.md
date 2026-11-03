# Resultados comparativos — EFL Championship

## Resumen de validación (últimos 190 partidos)

| Modelo | Accuracy | Log-Loss | RPS | Partidos |
|--------|----------|----------|-----|----------|
| Maher | 48.95% | 1.0426 | 0.2180 | 190 |
| Dixon-Coles | 51.58% | 1.0235 | 0.2152 | 190 |
| XGBoost | 47.37% | 1.0523 | 0.2187 | 190 |

## Parámetros del modelo optimizados

### Maher (Poisson estático)
- **w_goals**: 0.57188
- **w_shots_target**: 0.27192
- **w_shots_total**: 0.15620
- **train_neg_log_likelihood**: 0.9951051278139493

### Dixon-Coles (Poisson dinámico)
- **w_goals**: 0.57188
- **w_shots_target**: 0.27192
- **w_shots_total**: 0.15620
- **xi** (decaimiento temporal): 0.00890
- **rho** (correlación scores bajos): 0.00948
- **train_neg_log_likelihood**: 1.0568854303357904

### XGBoost (Gradient Boosting)
- **best_max_depth**: 2
- **best_learning_rate**: 0.02047163923555036
- **best_n_estimators**: 126
- **train_cv_logloss**: 1.0371420415003159

## Mejor estrategia de apuestas (Max ROI)

| Modelo | Margen | Kelly | Max Odd | Apuestas | Balance | ROI (%) |
|--------|--------|-------|---------|----------|---------|---------|
| Maher | 1.53 | 1.0 | 5.8 | 20 | 9.90 | 49.51 |
| Dixon-Coles | 1.52 | 1.0 | 9.5 | 19 | 6.56 | 34.55 |
| XGBoost | 1.16 | 0.01 | 2.6 | 20 | -0.01 | -0.03 |
