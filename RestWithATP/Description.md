## Description of this Intergation

This Integration is designed with a REST Adapter in Trigger mode with Single Parameter as Country ID(Ex: 52781). After passing the parameter into the integration it will take the corresponding 2-Digit ISO Code for that country from ATP Database. So the ATP End Point has been configured as Invoke Connection. And Lastly using the that retrieved two digit code it will invoke Readily avialable REST End Point over Internet with Address:
`https://restcountries.com/v3.1/alpha/IN`, which is eventually retun Country Information from that Country Id.

