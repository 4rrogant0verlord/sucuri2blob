<p align="center">
  <h2 align="center">Sucuri-2-BlobStorage</h2>
  <p>
  Script para transferir eventos del Sucuri Web Application Firewall (WAF) hacia Azure Blob Storage, en formato CSV.
  </p>
</p>

---

#### Requerimientos:

* [Python3.8+](https://www.python.org/downloads/)

#### Como ejecutar:

Ejecute:

```
python3 -m venv env
```

En Windows, corra:

```
env\Scripts\activate.bat
```

En Unix o MacOS, corra:

```
source env/bin/activate
```

Luego ejecute:

```
pip install -r requirements.txt
```

Finalmente:

```
python3 app.py
```

#### Configuración:

```python
AZURE_ACC_KEY = ...        # Cambiar a la llave de cuenta correspondiente.
AZURE_ACC_NAME = ...       # Cambiar al nombre de cuenta correspondiente.
container_name = ...       # Cambiar al nombre de blob container correspondiente.
SUCURI_SITES = [
    {
        "secret": "...",   # Añadir tantos API_SECRET como le sea necesario.
        ...
    }
]
```

#### Referencias:

https://waf.sucuri.net/?apidocs
https://docs.microsoft.com/en-us/python/api/overview/azure/storage-blob-readme?view=azure-python
https://github.com/Azure/azure-sdk-for-python/tree/main/sdk/storage/azure-storage-blob
