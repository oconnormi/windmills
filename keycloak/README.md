# Keycloak Extension

This extension installs both the `keycloak-operator` as well as the `keycloak-realm-operator` to allow for declarative management of keycloak during application testing. This is useful if an application helm chart supports the various keycloak CRDs for registering clients within keycloak.

## Requirements

* Cert-manager already installed in cluster

## Usage

```python
v1alpha1.extension_repo(name='windmills', url='https://github.com/oconnormi/windmills')

# Example for using the keycloak extension
v1alpha1.extension(name='keycloak', repo_name='windmills', repo_path='keycloak')
load('ext://keycloak', 'keycloak')

keycloak()
```

This will bootstrap both `keycloak-operator` and `keycloak-realm-operator`. A keycloak instance will also be provisioned so that a project can simply start creating realms, clients, etc right away.