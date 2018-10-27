# Datafloe

## import eclipse
1. Import Eclipse like a Maven project
1. Run as "Java Application" or "Dataflow pipelines"
1. Set Main Class "MinimalWordCount"
1. Configure "Properties > Google Cloud Platform > Cloud Dataflow"
    - Account
    - Project Id
    - Cloud Storage
    - Service account key


## Run locally
```bash
# eclipse "Run">"Run configurations..."
export export GOOGLE_APPLICATION_CREDENTIALS="";
mvn compile exec:java -Dexec.mainClass=org.apache.beam.examples.MinimalWordCount -Dexec.args="--output=./output/";
```

## Deploy
```bash
PROJECT_ID="";
STORAGE_BUCKET="";
mvn -Pdataflow-runner compile exec:java \
      -Dexec.mainClass=org.apache.beam.examples.WordCount \
      -Dexec.args="--project=${PROJECT_ID} \
      --stagingLocation=gs://${STORAGE_BUCKET}/staging/ \
      --output=gs://${STORAGE_BUCKET}/output \
      --runner=DataflowRunner";
```
