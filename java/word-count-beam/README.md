# datafloe

## Run locally
```bash
mvn compile exec:java -Dexec.mainClass=org.apache.beam.examples.WordCount -Dexec.args="--output=./output/";
```

## Deploy
```bash
mvn -Pdataflow-runner compile exec:java \
      -Dexec.mainClass=org.apache.beam.examples.WordCount \
      -Dexec.args="--project=${PROJECT_ID} \
      --stagingLocation=gs://${STORAGE_BUCKET}/staging/ \
      --output=gs://${STORAGE_BUCKET}/output \
      --runner=DataflowRunner";
```
