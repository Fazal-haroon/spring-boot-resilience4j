# spring-boot-resilience4j
Spring boot, ServiceA, ServiceB and resilience4j
<br>
1 First of all, i create two services(serviceA and serviceB)
<br>
![image](https://user-images.githubusercontent.com/36573782/190924321-375335a2-8d58-4c69-b922-b53532bd044a.png)
<br>
2 I call get request of service A and indirect calling service B. In service a i added Resilience4j dependency. Also i added actuator and aop dependencies in service A
<br>
3 we define fallback method, whenever the service down the fallback invoke.
<br>
![image](https://user-images.githubusercontent.com/36573782/190925501-dd3bacdf-2850-44ef-ac4e-7d05d890cae7.png)
<br>
I just stop the service B so we get this fallback message
<br>
![image](https://user-images.githubusercontent.com/36573782/190925534-86455011-37d4-4fe4-9a06-102574a6b1da.png)
<br>
![image](https://user-images.githubusercontent.com/36573782/190925495-28e485ee-a565-4088-b8b0-74fdcbd7a1af.png)
<br>
Circuit breaker from closed to open again
<br>
![image](https://user-images.githubusercontent.com/36573782/190925750-df583914-e9f6-4b54-a2a4-20dc01288e52.png)
