# Links
## Pluralsight 
[CKAD - certification](https://app.pluralsight.com/explore/certifications/topics/kubernetes?examPrepId=6ae9cedf-075b-4314-b01b-ca1e023ee791)

### Courses
* [Application Design and Build for CKAD](https://app.pluralsight.com/library/courses/application-design-build-ckad-cert/table-of-contents)
* [Certified Kubernetes Application Developer Application Deployment](https://app.pluralsight.com/library/courses/ckad-deploying-applications-cert/table-of-contents) - [code](https://github.com/DanWahlin/ckad/tree/main/2%20Application%20Deployment)

## Kubernetes game
https://github.com/Aryan4266/k8squest

# My notes
* use expose

  `k expose deploy nginx-deploy --port=9000 --target-port=80 --type=NodePort --name=nginx-svc --dry-run=client -o yaml > svc.yaml`

* use edit - saving edit automatically applies

  ` k edit deploy/nginx-deploy`

* applying all files in folder

  `k apply -f ./`

* adding default namespace

  `k config set-context --current --namespace=dev`

* get all

  `k get all`

* setting some value

  `k set selector svc public-service "role=green"`

* edit in nano

  `KUBE_EDITOR="nano" k edit deploy web-app`

* change image in deployment

  `k set image deploy web-app nginx=nginx:1.23.1-alpine`

* adding annotation

  `k annotate deploy web-app kubernetes.io/change-cause="Changed to nginx: 1.23.1" --overwrite=true`

* rollout status

  `k rollout status deploy web-app`

* rollout history

  `k rollout history deploy biz-app`

* rollout undo

  `k rollout undo deploy biz-app`

* automatic scaling

  `kubectl autoscale deployment <name> --min=2 --max=10 --cpu-percent=70`

* get api versions

  `kubectl api-resources`

  
  
