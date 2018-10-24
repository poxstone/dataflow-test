# Dataflow examples

## run locally
```bash
mvn compile exec:java -Dexec.mainClass=com.poxstone.StarterPipeline -Dexec.args="--runner=DirectRunner";
```

## run dataflow service
```bash
mvn -Pdataflow-runner compile exec:java -Dexec.mainClass=com.poxstone.StarterPipeline -Dexec.args="--project=${PROJECT_ID} --runner=DataflowRunner";
```

