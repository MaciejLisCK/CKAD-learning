# Links
* [Pluralsight CKAD - certification](https://app.pluralsight.com/explore/certifications/topics/kubernetes?examPrepId=6ae9cedf-075b-4314-b01b-ca1e023ee791)
* [Kubernetes.io cheatsheet](https://kubernetes.io/docs/reference/kubectl/quick-reference/)
* [Reddit cheatsheet](https://github.com/SergeyFM/docs/blob/main/kubernetes_commands_cheat_sheet_final.txt)
* [Reddit how k8s works easy explaination video](https://www.reddit.com/r/kubernetes/comments/x1ppc4/k8s_irl/)

### Courses
* [Application Design and Build for CKAD](https://app.pluralsight.com/library/courses/application-design-build-ckad-cert/table-of-contents)
* [Certified Kubernetes Application Developer Application Deployment](https://app.pluralsight.com/library/courses/ckad-deploying-applications-cert/table-of-contents) - [code](https://github.com/DanWahlin/ckad/tree/main/2%20Application%20Deployment)

## Kubernetes game
https://github.com/Aryan4266/k8squest

## Exam braindump
* https://youtu.be/SFXdXwTvruc?si=d3JKNP50Hh-n1Qq

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

  `k set image deployment web-app nginx=nginx:1.23.1-alpine`

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

* get metrics

  `kubectl top --raw /api/v1/nodes/<NODE_NAME>/proxy/metrics/resource > nodemetrics.txt`

* check rbac perrmission

  `k auth can-i list pods --as=system:serviceaccount:k8squest:pod-reader`

* documentation

  `k explain pod.spec.tolerations`
  
