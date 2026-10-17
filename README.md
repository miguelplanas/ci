# ci

Workflows compartidos por las apps del homelab. Un arreglo aquí vale para todas
las apps a la vez (se llaman con `@main`).

- `deploy-dokploy.yml`: entra al tailnet, lanza el despliegue en Dokploy y
  espera a que acabe de verdad (`done` o `error`).
- `guard.yml`: check obligatorio del merge automático. Falla si el PR toca datos,
  autenticación, la CI o borra código de la app, salvo con la etiqueta
  `ok-miguel`.

Uso: ver la cabecera de cada fichero y la plantilla `miguelplanas/plantilla-app`.
Repo público a propósito (las apps públicas no pueden llamar a workflows de un
repo privado). No contiene secretos: llegan con `secrets: inherit`.
