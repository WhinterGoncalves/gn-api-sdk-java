# SDK GERENCIANET FOR JAVA

Sdk for Gerencianet Pagamentos' API.
For more informations about parameters and values, please refer to [Gerencianet](http://gerencianet.com.br) documentation.

**Em caso de d�vidas, voc� pode verificar a [Documenta��o](https://docs.gerencianet.com.br) da API na Gerencianet e, necessitando de mais detalhes ou informa��es, entre em contato com nossa consultoria t�cnica, via nossos [Canais de Comunica��o](https://gerencianet.com.br/central-de-ajuda).**


[![Build Status](https://travis-ci.org/gerencianet/gn-api-sdk-java.svg?branch=master)](https://travis-ci.org/gerencianet/gn-api-sdk-java)

## Requirements
* Java >= 8.0

## Getting started
Require the module and packages:
```java
import br.com.gerencianet.gnsdk.Gerencianet;
import br.com.gerencianet.gnsdk.exceptions.GerencianetException;

```
Although the web services responses are in json format, the sdk will convert any server response to a JSONObject or a Map<String, Object>. The code must be within a try-catch and exceptions can be handled as follow:
```
```java
try {
  /* code */
} catch(GerencianetException e) {
  /* Gerencianet's api errors will come here */
} catch(Exception ex) {
  /* Other errors will come here */
}
```

### For development environment
Instantiate the module passing using your client_id, client_secret and sandbox equals true:
```java
JSONObject options = new JSONObject();
options.put("client_id", "client_id");
options.put("client_secret", "client_secret");
options.put("sandbox", true);
];

Gerencianet gn = new Gerencianet($options);
```
Or

```java
Map<String, Object> options = new HashMap<String, Object>();
options.put("client_id", "client_id");
options.put("client_secret", "client_secret");
options.put("sandbox", true);
];

Gerencianet gn = new Gerencianet($options);
```

### For production environment
To change the environment to production, just set the third sandbox to false:
```java
JSONObject options = new JSONObject();
options.put("client_id", "client_id");
options.put("client_secret", "client_secret");
options.put("sandbox", false);
];

Gerencianet gn = new Gerencianet($options);
```
Or

```java
Map<String, Object> options = new HashMap<String, Object>();
options.put("client_id", "client_id");
options.put("client_secret", "client_secret");
options.put("sandbox", false);
];

Gerencianet gn = new Gerencianet($options);
```

## Running tests

To run the test suite with coverage:

```
./mvn jacocoTestReport
```

## Additional Documentation

#### Charges
- [Creating charges](/docs/CHARGE.md)
- [Paying a charge](/docs/CHARGE_PAYMENT.md)
- [Detailing charges](/docs/CHARGE_DETAIL.md)
- [Updating informations](/docs/CHARGE_UPDATE.md)
- [Resending billet](/docs/RESEND_BILLET.md)
- [Adding information to charge's history](/docs/CHARGE_CREATE_HISTORY.md)

#### Carnets

- [Creating carnets](/docs/CARNET.md)
- [Detailing carnets](/docs/CARNET_DETAIL.md)
- [Updating informations](/docs/CARNET_UPDATE.md)
- [Resending the carnet](/docs/CARNET_RESEND.md)
- [Resending carnet parcel](/docs/CARNET_RESEND_PARCEL.md)
- [Adding information to carnet's history](/docs/CARNET_CREATE_HISTORY.md)
- [Canceling the carnet](/docs/CARNET_CANCEL.md)
- [Canceling carnet parcel](/docs/CARNET_CANCEL_PARCEL.md)

#### Subscriptions

- [Creating subscriptions](/docs/SUBSCRIPTION.md)
- [Setting the payment method](/docs/SUBSCRIPTION_PAYMENT.md)
- [Detailing subscriptions](/docs/SUBSCRIPTION_DETAIL.md)
- [Updating informations](/docs/SUBSCRIPTION_UPDATE.md)
- [Listing plans](/docs/PLAN_LIST.md)

#### Marketplace

- [Creating a marketplace](/docs/MARKETPLACE.md)

#### Notifications

- [Getting notifications](/docs/NOTIFICATION.md)

#### Payments

- [Getting the payment data](/docs/PAYMENT_DATA.md)

## Changelog

[CHANGELOG](CHANGELOG.md)

## License ##
[MIT](LICENSE)
