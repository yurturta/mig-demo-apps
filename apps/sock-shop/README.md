# Sock Shop

An e-commerce website that sells socks.

## Installation

Login to your OpenShift cluster. 

To deploy:

```bash
./deploy.sh
```

To remove:

```bash
./destroy.sh
```

`manifests` directory contains definitions for different resources required by the app. `manifest.yaml` is just a collection of all those definitions. 

You may edit individual definitions for different app resources. To create an updated `manifest.yml` after updating individual resource definitions :

```bash
./build.sh
```

This will combine all YAMLs and create an updated `manifest.yaml`.

## Usage

After successful installation, the app should be exposed at a public URL. Wait for 4-5 minutes for all the services to start.

To get the url to the frontend:

```bash
oc get route -n sock-shop front-end -o go-template='{{ .spec.host }}{{ println }}'
```

Visit the URL and order socks for free. Deliveries not guaranteed! 




