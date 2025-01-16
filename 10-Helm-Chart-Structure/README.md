# Understand Helm Chart Folder Structure

## Step-01: Introduction
- Understand Helm Chart Folder Structure

## Step-02: Helm Create Chart
```t
# Helm Create Chart
helm create <CHART-NAME>
helm create basechart
Observation: 
1. It will create a Helm Chart template 
2. We can call it like a helm chart created from a default starter chart
```

## Step-03: Helm Chart Structure
```
└── basechart
    ├── .helmignore
    ├── Chart.yaml
    ├── LICENSE
    ├── README.md
    ├── charts
    ├── templates
    │   ├── NOTES.txt
    │   ├── _helpers.tpl
    │   ├── deployment.yaml
    │   ├── hpa.yaml
    │   ├── ingress.yaml
    │   ├── service.yaml
    │   ├── serviceaccount.yaml
    │   └── tests
    │       └── test-connection.yaml
    └── values.yaml
```

**Chart.yaml** file will have the details of helm charts like name, description etc.  
**charts/** directory will have dependencies mentioned in our Chart.yaml. Dependencies example - let's say we are building an app and we need mysql db, so that will become dependency.   

**_helpers.tpl** : this file is used to create reusable parts in our charts. note: any file inside templates/ directry which starts with underscore _ won't create a K8s object.
