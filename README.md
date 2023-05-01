# PostgreSQL Kubernates Manifests ⚙️



- kubernates  manifests for deploying postgres deployment with persistence storage.
- kubernates manifests are managed by ***Kustomize***

## Requirement

1. kubectl 
2. kustomize v5.0.0 or above

## Installation

- make a directory</br>
<pre>mkdir < dir_name > </pre> 
- iniate a kustomization file</br>
<pre> kustomize init </pre>
***or*** </br>
<pre>touch kustomization</pre>
- add below tags
<pre>
resources:
- github.com/kuMunasinghe/postgresql-kubernetes-deployment?ref= < tag >

namespace: < namespace >
namePrefix: < app_name >
configMapGenerator:
- name: postgres-init-script
  files:
  - init.sql= < db init sql file >
  behavior: replace

</pre>






###### ! default psql password --> postgresql 
