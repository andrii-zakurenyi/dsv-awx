# DSV Lookup in AWX

## Execution Environment

You can use Execution Environment that I created:

https://github.com/andrii-zakurenyi/dsv-awx/pkgs/container/ee-with-dsv-sdk

```
ghcr.io/andrii-zakurenyi/ee-with-dsv-sdk:0.1.0
```

Follow next steps to create your own Execution Environment with a "community.general"
collection and a DSV SDK version "v0.0.1" for Python installed. Note that all commands
should be executed from the project root directory.

1. Create a virtual environment:

    ```
    python3 -m venv venv
    ```

2. Activate a virtual environment:

    ```
    source venv/bin/activate
    ```

3. Install ansible-builder

    ```
    pip install ansible-builder
    ```

4. Build the image:

    ```
    ansible-builder build --tag ee-with-dsv-sdk --container-runtime docker
    ```

5. Done. Now cleanup: exit from virtual environemnt, remove venv and context directories.

    ```
    deactivate
    ```

    ```
    rm -rf venv context
    ```
