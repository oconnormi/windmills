# Tilt Extensions

Add the following to a 'Tiltfile' to use extensions from this repo:

```python
v1alpha1.extension_repo(name='windmills', url='file:///home/mike/workspace/windmills')

# Example for using the keycloak extension
v1alpha1.extension(name='keycloak', repo_name='windmills', repo_path='keycloak')
load('ext://keycloak', 'keycloak')
```