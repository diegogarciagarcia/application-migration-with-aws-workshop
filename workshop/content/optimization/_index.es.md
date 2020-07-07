+++
title = "Optimizacion"
weight = 40
pre = "<b>4. </b>"

+++


Enhorabuena, si has llegado aqui has conseguido migrar una aplicación de commercio electrónico a AWS y ahora puedes mirar como optimizar la arquitectura para hacerlo incluso mas seguro, de alto rendimiento, resistente y ¡que use la infraestructura de AWS eficientemente!

Mas abajo encontrara ideas que puede considerar <a href="https://aws.amazon.com/architecture/well-architected/" target="_blank">5 Pilares del Marco de Buena Arquitectura de AWS</a> - Excelencia Operativa, Seguridad, Fiabilidad, Eficacia del rendimiento y Optimizacion de costes.

Tambien puede aprender mas sobre **Marco de Buena Arquitectura** viendo el video de abajo.
<center>
<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/MfxF-FYEFjY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>

### Excelencia Operativa

- Configura un a <a href="https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Dashboards.html" target="_blank"> informe de CloudWatch </a> para monitorizar tus recursos en una unica vista, incluso a traves de varias regiones de AWS.
- Configura un <a href="https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-create-and-update-a-trail.html" target="_blank">registro persistente de CloudTrail</a> para ser capaz de monitorizar, auditar y alertar que esta pasando en tus cuentas de AWS

### Seguridad  
- Cambia a HTTPS con <a href="https://aws.amazon.com/certificate-manager/" target="_blank">AWS Certificate Manager</a> gestiona certificados SSL/TLS para encriptar datos de cliente en transito (¡los certificados ya se proporcionan en este laboratorio!) 
- <a href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSEncryption.html" target="_blank">Encripta volumenes EBS</a> para proteger los datos del cliente en reposo
- Habilita <a href="https://aws.amazon.com/waf/"  target="_blank">AWS Web Application Firewall (AWS WAF)</a> para proteger tu aplicacion web de ataques conocidos (puedes hacerlo aqui <a href="https://aws.amazon.com/blogs/aws/aws-web-application-firewall-waf-for-application-load-balancers/" target="_blank">Application Load Balancer</a> o incluso mejor en <a href="https://docs.aws.amazon.com/waf/latest/developerguide/cloudfront-features.html" target="_blank">Amazon CloudFront distribution</a>)
- Use <a href="https://aws.amazon.com/guardduty/" target="_blank">Amazon GuardDuty</a> to protect your AWS account and workloads with intelligent threat detection and continuous monitoring

### Reliability
- Configure an <a href="https://docs.aws.amazon.com/elasticloadbalancing/latest/application/create-application-load-balancer.html" target="_blank">Application Load Balancer</a> to distribute Webserver traffic across multiple Availability Zones
- Configure <a href="https://docs.aws.amazon.com/autoscaling/ec2/userguide/GettingStartedTutorial.html" target="_blank">Amazon EC2 Auto Scaling Group</a> to enable auto-healing in case Webserver instances go down and to handle changing customer load
- Use <a href="https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-working-with.html" target="_blank">Amazon CloudFront</a> - a fast Content Distribution Network that securely delivers data to customers globally with low latency and high transfer speeds, integrating seamlessly with <a href="https://aws.amazon.com/shield/" target="_blank">AWS Shield</a> for DDoS mitigation.

### Performance Efficiency
- Deploy <a href="https://docs.aws.amazon.com/efs/latest/ug/getting-started.html" target="_blank">Amazon Elastic File System</a> to handle changes of files on Webservers
- Use <a href="https://aws.amazon.com/blogs/networking-and-content-delivery/amazon-s3-amazon-cloudfront-a-match-made-in-the-cloud/" target="_blank">Amazon CloudFront with AWS S3</a> as custom origin to distribute static content for lower latency for your customers and lower cost

### Cost optimization
- Use <a href="https://aws.amazon.com/ec2/spot/" target="_blank">Amazon EC2 Spot instances</a> - select machine type using <a href="https://aws.amazon.com/ec2/spot/instance-advisor/" target="_blank">EC2 Spot Advisor</a>, some instances allow for **90% savings** with <5% interruption frequency
- Use the most <a href="https://aws.amazon.com/ec2/spot/pricing/" target="_blank">cost-optimized machine types</a>

### Reference architecture

Diagram below depicts a reference architecture of the solution, with all components listed above deployed.

![Reference Architecture](/opt/aws-ref-arch.png)

For more details see the <a href="https://github.com/aws-samples/aws-refarch-wordpress" target="_blank">Reference Architecture for Wordpress on AWS</a>!
