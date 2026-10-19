# gitops-demo

The ONE git repo Argo CD watches for Experiment X. `deploy/` is the entire
desired state — a namespace, an nginx Deployment at `replicas: 2`, and a
Service. Nothing else in this repo matters to Argo CD.

Push this to a public GitHub repo (e.g. `github.com/vkhanna18/gitops-demo`)
before the presentation — Argo CD needs a URL it can clone. A private repo
works too, but needs a deploy key or token configured in Argo CD, which is
one more thing that can fail live; public is simpler for a 10-minute slot.

During the demo, the only change ever made to this repo is editing
`deploy/nginx-deployment.yaml`'s `replicas:` field and pushing — see
`../demo.sh` for exactly when.
