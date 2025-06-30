# Proyecto 1: Plataforma de despliegue continuo local (Mini-GitOps)

* Alumno: Joel Benjamin Seminario Serna
* Código: 20210056G
* Correo institucional: joel.seminario.s@uni.pe
* Enlace del repositorio grupal: https://github.com/AlemEsv/pc4-grupo4-tema1

## Videos:
* Carpeta de videos grupal: https://drive.google.com/drive/folders/17LHca0hkqFgUesVOaw6JTp_Z-2xtlv5w?usp=sharing
  
* Carpeta de videos individual: https://drive.google.com/drive/folders/1nWvkis3guQdvijOzQ0AWN8PKXirCHmwL?usp=sharing
  
- [**Video Sprint 1**](https://drive.google.com/file/d/1-30PtTELNW6knPTHX6XkzuL55M5NAowj/view?usp=sharing)

- [**Video Sprint 2**](https://drive.google.com/file/d/1qTVA4tNJcs28HX3VMUCkSAreZabxeLB3/view?usp=sharing)

- [**Video Sprint 3**](https://drive.google.com/file/d/1zNo3TUqEw7CRpQc2WXZ7LAFjyRJsdEKS/view?usp=sharing)

En el sprint desarrollé el script git_monitor.py que se encarga de detectar cambios entre los commits locales y remotos con el objetivo de automatizar el flujo de despliegue. Esto nos ayudo a que se integre más adelante con los manifiestos de la aplicación.

Para el sprint 2 y 3 continué mejorando git_monitor.py, agregándole la lógica para hacer git pull y aplicar los manifiestos automáticamente si se detectaban cambios. También implementé pruebas unitarias para validar su comportamiento desde etapas tempranas y, posteriormente, desarrollé pruebas de integración en Minikube (integration-tests.py) para asegurar que todo funcionara correctamente en un entorno real. Ademas, documenté el proceso para facilitar su uso por parte del equipo.

## Instalación

``` 
git clone https://github.com/AlemEsv/app-manifests.git
cd app-manifests
python3 -m venv .venv
source .venv/Scripts/activate
pip install -r requirements.txt
```

## Ejecución de Scripts

* git_monitor
``` 
cd .\pc4-grupo4-tema1\scripts\
minikube start --driver=docker
kubectl apply -f ./app-manifests/manifests/deployment.yaml
kubectl apply -f ./app-manifests/manifests/service.yaml
python .\git_monitor.py
``` 
## Ejecución de pruebas unitarias

* test_git_monitor
``` 
cd .\pc4-grupo4-tema1\tests\unit\
pytest .\test_git_monitor.py
``` 

* integration-test 
``` 
cd .\pc4-grupo4-tema1\tests\integration\
pytest .\integration-tests.py
``` 


## Videos grupales

- [**Video Sprint 1**](https://drive.google.com/file/d/1RCYpoSqdk2u3IU5WEPXr7lNXgw5CSirs/view?usp=sharing)

- [**Video Sprint 2**](https://drive.google.com/file/d/1XCiLPSQDIrydoPC9nj7fgx0n35-fumKQ/view?usp=sharing)

- [**Video Sprint 3**](https://drive.google.com/file/d/1-Z0oBtFXMEhAb5o0QYTvQhvlcvZfD968/view?usp=sharing)
- 
