# Links
## Pluralsight 
[CKAD - certification](https://app.pluralsight.com/explore/certifications/topics/kubernetes?examPrepId=6ae9cedf-075b-4314-b01b-ca1e023ee791)

### Courses
* [Application Design and Build for CKAD](https://app.pluralsight.com/library/courses/application-design-build-ckad-cert/table-of-contents)
* [Certified Kubernetes Application Developer Application Deployment](https://app.pluralsight.com/library/courses/ckad-deploying-applications-cert/table-of-contents)


# My notes
* use expose

  `k expose deploy nginx-deploy --port=9000 --target-port=80 --type=NodePort --name=nginx-svc --dry-run=client -o yaml > svc.yaml`

* use edit - saving edit automatically applies

  ` k edit deploy/nginx-deploy`