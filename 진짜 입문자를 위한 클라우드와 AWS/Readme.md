# 📕 

클라우드란 컴퓨터 리소스를 직접 구매하지 않고 인터넷을 통해서 서비스로 제공받는 것을 의미합니다.

컴퓨팅, 스토리지, 네트워크 - 클라우드의 요소

infrastucte as a Service = Iaas(아이아스)

서버(=host computer)

* AWS를 사용한다면

컴퓨팅 - EC2 : cpu + memory
스토리지 - EBS : 블록저장장치(ssd) S3 - block device
네트워크 - VPC Route53

돈보다 중요한 것은 탄력성과 내구도, 안정성

https://calculator.s3.amazonaws.com/index.html

탄력성 : 서비스 규모에 맞게 IT 인프라를 확장 / 축소할 수 있는가?
내구성 : 오류 및 사고발생 시점에서 데이터가 안전하게 저장되는가?
안정성 : 다운타임 / 유지보수시간을 최소화하고 서비스가 정상적으로 유지되는가?

가용성 : 서비스가 항상 사용 가능한지 나타내는 지표

EBS : EC2와 연결해서 사용하는 SSD 같은 서비스
S3: 드롭박스처럼 파일 업로드 / 다운로드가 가능한 인터넷 저장 서비스

aws s3는
폴더가 아니라 접두어라고 합니다.

인터넷 = 인터네트워크 
인터넷 프로토콜(TCP / IP)를 통해 연결된 글로벌 네트워크
요즘은 www(=world wide web) = 인터넷이라고 합니다.

네트워크에서 서비스를 요청하는 기기를 클라이언트라고 합니다.
서비스를 제공해주는 기기를 서버라고 합니다.

IP : 4byte : 각 기기에 부여되는 고유한 번호
url : IP에 대응되는 고유한 주소 식별자
DNS: Domain Name system : url을 IP로 바꿔줍니다.
서버 네트워크 : 서비스하는 쪽의 서버들이 연결되어있는 망(사설망)

route53 : aws에서 제공해주는 DNS 서비스
리젼, cloud form -> cdn 서비스 -> pop

내부 네트워크 중 일부망은 인터넷과 연결 = DMZ

AWS Virtual Private Cloud : 가상 사설 네트워크

public subnet : 웹서버, 메일서버
private subnet : 데이터베이스, 보안 데이터, 백업 데이터 등

3 tier web application architecture

서버리스 : 서버가 없는 것처럼 자동으로 사용할 수 있습니다.

계정관리 : IAM
컴퓨팅 : EC2, Lambda, ECS
네트워크 : VPC, Route53, CloudFront
저장 : S3
데이터베이스 : RDS
모니터링 : CloudWatch, CloudTrail
기타 : SNS, SES, SQS, CloudFormation
