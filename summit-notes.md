RedHat Summit 2026

Faster Containers

* Use good containerfile hygeine, least changing stuff lower down
* Chunkah
    * https://github.com/coreos/chunkah
    * Context aware dockerfile, split content into defined layers
    * Also works with zstd:chunked
    * After built then use chunkah to turn into better, more smaller layers
* Use Zstd-chunked
    * Cli settings
    * Better compression for images
    * Faster pull time for automation, rancher review apps
    * Check if podman, jfrog, and rwncher can push it/support

Kubernetes 

* Everything/everyone going kube, we need to! And it’s my appraisal goal for this year 😁
* Zarf
* Skaffold can convert compose files
* Workflow
    * Devs can use compose
    * Integration testing can use skaffold which can make k8s based on compose
    * Release is zarf

DSO - RHADS

* RHDH - redhat developer hub - omni
* RHRAS - code signing
* RHTPA - scanning

Omni

* Make Developer onboarding for microservice architecture 
* Plugins
    * Kubernetes backend?
* Template makes repo, devspaces, pipelines, gitops

Code signing 

* Sigstore
* Git sign
* Cosign
* TUF
* Fulcio
* Rekor
* Enable tas-git-config in devspaces to enable gitsign

Security 

* Enforcing code signing
* Enforcing certain level of security 
* Can’t pull images if too bad
* Scanning images in rancher

Edge

* Device Edge
    * Immutable OS for running containers 
    * Would get deployed to ABITTs/ITSes
* Edge Manager
    * Every customer would need an edge manager in the airgapped setup
    * Move the new software to the edge manager, then edge devices checkin and pull updates
* SHIELD Project
    * Non technical folks, could make bootc image with OS and app containers
    * Deploy hardened OS
* MicroShift

Red Hat Hardened Images

* Free, check them out

Ai

* AI Agents
    * Kagenti
* vLLM - CPU only mode in rancher to test
* Kaiden - Use coding agents in isolated sandboxes

Podman Development

* Locally and remote development coexist among companies 
* Timeline from Amadeus
    * Vagrant VM with docker and openshift. Fast but hard to support VMs.
    * Then Docker desktop with kind. Easy to setup, but no file sync or true openshift.
    * Then Podman desktop with kind
    * Latest is local podman desktop with IDE. Then use helm, kind, podman desktop to test locally. CICD runs on k8s.  
