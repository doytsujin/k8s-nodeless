# k8s-nodeless

`k8s-nodeless` is a tiny tool to run a workload on Serverless runtime(ex: AWS Lambda) under a kubernetes manner.

## How to use

### 0. Create a Serverless function

Before using this tool, you should deploy your Serverless function by using any kind of deploy tools.


### 1. Create k8s manifest

Create kubernetes manifest which use k8s-nodeless Docker image.


```


```

Note: if you use AWS eks, need IAMServiceAccount to execute Lambda.

```
eksctl create iamserviceaccount --name lambda-execute --cluster sampleprj-stg-1 \
--attach-policy-arn arn:aws:iam::aws:policy/service-role/AWSLambdaBasicExecutionRole \
--approve
```

### 2. Run a Job with kurbernetes manner

```
$ kubectl apply -f lambda_job.yaml
```

## License

Apache License

