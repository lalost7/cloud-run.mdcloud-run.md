# Práctica: Serverless Containers con Google Cloud Run

## Objetivo

Realizar el despliegue de una aplicación utilizando Google Cloud Run mediante la herramienta de línea de comandos gcloud CLI.

## Configuración de región

```bash
gcloud config set run/region us-central1
```

## Despliegue del contenedor

```bash
gcloud run deploy srv-web-estudiante \
--image=gcr.io/cloudrun/hello \
--allow-unauthenticated \
--max-instances=3
```

## Explicación de parámetros

* `--allow-unauthenticated`: permite que cualquier usuario pueda acceder al servicio mediante una URL pública HTTPS sin necesidad de autenticación.
* `--max-instances=3`: establece un límite máximo de tres instancias para controlar el escalamiento automático y evitar costos innecesarios.

## Resultado obtenido

Se realizó la configuración de la región y se ejecutó el comando de despliegue del contenedor en Google Cloud Run. Sin embargo, el proceso no pudo completarse debido a restricciones relacionadas con la configuración y validación de la cuenta de facturación de Google Cloud. Como consecuencia, no fue posible generar la URL pública del servicio ni verificar su funcionamiento desde un navegador web.

## Conclusión

Google Cloud Run es una plataforma Serverless que permite ejecutar aplicaciones contenidas en imágenes Docker sin necesidad de administrar servidores o infraestructura. Entre sus principales ventajas se encuentran el escalamiento automático, la alta disponibilidad y el modelo de pago por uso, lo que facilita el despliegue eficiente de aplicaciones modernas en la nube.

## Fuentes

* Google Cloud. (s. f.). *Cloud Run Documentation*. https://cloud.google.com/run/docs
* Google Cloud. (s. f.). *Deploying container images to Cloud Run*. https://cloud.google.com/run/docs/deploying
* Google Cloud SDK. (s. f.). *gcloud CLI Reference*. https://cloud.google.com/sdk/gcloud
* Google Cloud. (s. f.). *Cloud Run Quickstart*. https://cloud.google.com/run/docs/quickstarts/build-and-deploy
