# Dataflow examples

## eclipse
1. Install Google Dataflow Plugin
1. Import like Maven project
1. Try run "Dataflow pipelines" or "Java application" and configure
1. Set Main Class "StarterPipeline"
1. Configure "Properties > Google Cloud Platform > Cloud Dataflow"
    - Account
    - Project Id
    - Cloud Storage
    - Service account key

## run locally
```bash
mvn compile exec:java -Dexec.mainClass=com.poxstone.StarterPipeline -Dexec.args="--runner=DirectRunner";
```

## run dataflow service
```bash
mvn -Pdataflow-runner compile exec:java -Dexec.mainClass=com.poxstone.StarterPipeline -Dexec.args="--project=${PROJECT_ID} --runner=DataflowRunner";
```

