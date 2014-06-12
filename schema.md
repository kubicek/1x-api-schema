Overview

## Contact
FIXME

### Attributes
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td><strong>authorization_key</strong></td>
    <td><em>string</em></td>
    <td>autorizační klíč kontaktu</td>
    <td><code>"SeCr3t:T0k3n"</code></td>
  </tr>
  <tr>
    <td><strong>city</strong></td>
    <td><em>string</em></td>
    <td>město</td>
    <td><code>"Praha"</code></td>
  </tr>
  <tr>
    <td><strong>country</strong></td>
    <td><em>string</em></td>
    <td>kód státu</td>
    <td><code>"CZ"</code></td>
  </tr>
  <tr>
    <td><strong>created_at</strong></td>
    <td><em>date-time</em></td>
    <td>when contact was created</td>
    <td><code>"2012-01-01T12:00:00Z"</code></td>
  </tr>
  <tr>
    <td><strong>email</strong></td>
    <td><em>string</em></td>
    <td>e-mail</td>
    <td><code>"info@kraxnet.cz"</code></td>
  </tr>
  <tr>
    <td><strong>fax</strong></td>
    <td><em>string</em></td>
    <td>fax</td>
    <td><code>420.2201992</code></td>
  </tr>
  <tr>
    <td><strong>first_name</strong></td>
    <td><em>string</em></td>
    <td>jméno</td>
    <td><code>"Jiří"</code></td>
  </tr>
  <tr>
    <td><strong>hide</strong></td>
    <td><em>string</em></td>
    <td>skryté údaje</td>
    <td><code>""</code></td>
  </tr>
  <tr>
    <td><strong>id</strong></td>
    <td><em>string</em></td>
    <td>identifikátor kontaktu</td>
    <td><code>"KRAXNET"</code></td>
  </tr>
  <tr>
    <td><strong>ident</strong></td>
    <td><em>string</em></td>
    <td>hodnota identifikátoru</td>
    <td><code>26460335</code></td>
  </tr>
  <tr>
    <td><strong>ident_type</strong></td>
    <td><em>string</em></td>
    <td>typ identifikátoru (OP,Pas,MPSV,IC,Datum narození)</td>
    <td><code>"IC"</code></td>
  </tr>
  <tr>
    <td><strong>last_name</strong></td>
    <td><em>string</em></td>
    <td>příjmení</td>
    <td><code>"Kubíček"</code></td>
  </tr>
  <tr>
    <td><strong>notify_email</strong></td>
    <td><em>string</em></td>
    <td>e-mail pro oznámení</td>
    <td><code>"notify@kraxnet.cz"</code></td>
  </tr>
  <tr>
    <td><strong>organization</strong></td>
    <td><em>string</em></td>
    <td>firma</td>
    <td><code>"KRAXNET s.r.o."</code></td>
  </tr>
  <tr>
    <td><strong>phone</strong></td>
    <td><em>string</em></td>
    <td>telefon</td>
    <td><code>420.220199201</code></td>
  </tr>
  <tr>
    <td><strong>state</strong></td>
    <td><em>string</em></td>
    <td>region</td>
    <td><code>""</code></td>
  </tr>
  <tr>
    <td><strong>street</strong></td>
    <td><em>string</em></td>
    <td>ulice, číslo popisné</td>
    <td><code>"Kamenická 26"</code></td>
  </tr>
  <tr>
    <td><strong>tld</strong></td>
    <td><em>string</em></td>
    <td>doména nejvyššího řádu (TLD)</td>
    <td><code>"cz"</code></td>
  </tr>
  <tr>
    <td><strong>updated_at</strong></td>
    <td><em>date-time</em></td>
    <td>when contact was updated</td>
    <td><code>"2012-01-01T12:00:00Z"</code></td>
  </tr>
  <tr>
    <td><strong>vat</strong></td>
    <td><em>string</em></td>
    <td>DIČ</td>
    <td><code>"CZ26460335"</code></td>
  </tr>
  <tr>
    <td><strong>zip</strong></td>
    <td><em>string</em></td>
    <td>poštovní směrovací číslo</td>
    <td><code>17000</code></td>
  </tr>
</table>

### Contact Check
Služba pro ověření dostupnosti kontaktu.

```
POST /contacts/check
```

#### Optional Parameters
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td><strong>id</strong></td>
    <td><em>string</em></td>
    <td>identifikátor kontaktu</td>
    <td><code>"KRAXNET"</code></td>
  </tr>
</table>


#### Curl Example
```term
$ curl -n -X POST https://api.hello.com/contacts/check
-H "Content-Type: application/json" \
-d '{"id":"KRAXNET"}'
```


#### Response Example
```
HTTP/1.1 200 OK
```
```json
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "registry_object_name": "kraxnet.cz",
  "object_type": "domain",
  "request_type": "check",
  "content": "{}",
  "status": "successful"
}
```

### Contact Register
Služba pro vytvoření nového kontaktu.

```
POST /contacts/register
```

#### Optional Parameters
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td><strong>authorization_key</strong></td>
    <td><em>string</em></td>
    <td>autorizační klíč kontaktu</td>
    <td><code>"SeCr3t:T0k3n"</code></td>
  </tr>
  <tr>
    <td><strong>city</strong></td>
    <td><em>string</em></td>
    <td>město</td>
    <td><code>"Praha"</code></td>
  </tr>
  <tr>
    <td><strong>country</strong></td>
    <td><em>string</em></td>
    <td>kód státu</td>
    <td><code>"CZ"</code></td>
  </tr>
  <tr>
    <td><strong>email</strong></td>
    <td><em>string</em></td>
    <td>e-mail</td>
    <td><code>"info@kraxnet.cz"</code></td>
  </tr>
  <tr>
    <td><strong>fax</strong></td>
    <td><em>string</em></td>
    <td>fax</td>
    <td><code>420.2201992</code></td>
  </tr>
  <tr>
    <td><strong>first_name</strong></td>
    <td><em>string</em></td>
    <td>jméno</td>
    <td><code>"Jiří"</code></td>
  </tr>
  <tr>
    <td><strong>hide</strong></td>
    <td><em>string</em></td>
    <td>skryté údaje</td>
    <td><code>""</code></td>
  </tr>
  <tr>
    <td><strong>id</strong></td>
    <td><em>string</em></td>
    <td>identifikátor kontaktu</td>
    <td><code>"KRAXNET"</code></td>
  </tr>
  <tr>
    <td><strong>ident</strong></td>
    <td><em>string</em></td>
    <td>hodnota identifikátoru</td>
    <td><code>26460335</code></td>
  </tr>
  <tr>
    <td><strong>ident_type</strong></td>
    <td><em>string</em></td>
    <td>typ identifikátoru (OP,Pas,MPSV,IC,Datum narození)</td>
    <td><code>"IC"</code></td>
  </tr>
  <tr>
    <td><strong>last_name</strong></td>
    <td><em>string</em></td>
    <td>příjmení</td>
    <td><code>"Kubíček"</code></td>
  </tr>
  <tr>
    <td><strong>notify_email</strong></td>
    <td><em>string</em></td>
    <td>e-mail pro oznámení</td>
    <td><code>"notify@kraxnet.cz"</code></td>
  </tr>
  <tr>
    <td><strong>organization</strong></td>
    <td><em>string</em></td>
    <td>firma</td>
    <td><code>"KRAXNET s.r.o."</code></td>
  </tr>
  <tr>
    <td><strong>phone</strong></td>
    <td><em>string</em></td>
    <td>telefon</td>
    <td><code>420.220199201</code></td>
  </tr>
  <tr>
    <td><strong>state</strong></td>
    <td><em>string</em></td>
    <td>region</td>
    <td><code>""</code></td>
  </tr>
  <tr>
    <td><strong>street</strong></td>
    <td><em>string</em></td>
    <td>ulice, číslo popisné</td>
    <td><code>"Kamenická 26"</code></td>
  </tr>
  <tr>
    <td><strong>tld</strong></td>
    <td><em>string</em></td>
    <td>doména nejvyššího řádu (TLD)</td>
    <td><code>"cz"</code></td>
  </tr>
  <tr>
    <td><strong>vat</strong></td>
    <td><em>string</em></td>
    <td>DIČ</td>
    <td><code>"CZ26460335"</code></td>
  </tr>
  <tr>
    <td><strong>zip</strong></td>
    <td><em>string</em></td>
    <td>poštovní směrovací číslo</td>
    <td><code>17000</code></td>
  </tr>
</table>


#### Curl Example
```term
$ curl -n -X POST https://api.hello.com/contacts/register
-H "Content-Type: application/json" \
-d '{"tld":"cz","id":"KRAXNET","organization":"KRAXNET s.r.o.","first_name":"Jiří","last_name":"Kubíček","email":"info@kraxnet.cz","phone":420.220199201,"fax":420.2201992,"ident_type":"IC","ident":26460335,"street":"Kamenická 26","city":"Praha","zip":17000,"country":"CZ","state":"","vat":"CZ26460335","authorization_key":"SeCr3t:T0k3n","notify_email":"notify@kraxnet.cz","hide":""}'
```


#### Response Example
```
HTTP/1.1 200 OK
```
```json
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "registry_object_name": "kraxnet.cz",
  "object_type": "domain",
  "request_type": "check",
  "content": "{}",
  "status": "successful"
}
```

### Contact Transfer
Služba pro změnu registrátora kontaktu na 1X.

```
POST /contacts/transfer
```

#### Optional Parameters
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td><strong>authorization_key</strong></td>
    <td><em>string</em></td>
    <td>autorizační klíč kontaktu</td>
    <td><code>"SeCr3t:T0k3n"</code></td>
  </tr>
  <tr>
    <td><strong>id</strong></td>
    <td><em>string</em></td>
    <td>identifikátor kontaktu</td>
    <td><code>"KRAXNET"</code></td>
  </tr>
</table>


#### Curl Example
```term
$ curl -n -X POST https://api.hello.com/contacts/transfer
-H "Content-Type: application/json" \
-d '{"id":"KRAXNET","authorization_key":"SeCr3t:T0k3n"}'
```


#### Response Example
```
HTTP/1.1 200 OK
```
```json
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "registry_object_name": "kraxnet.cz",
  "object_type": "domain",
  "request_type": "check",
  "content": "{}",
  "status": "successful"
}
```

### Contact Update
Služba pro změnu kontaktu.

```
POST /contacts/update
```

#### Optional Parameters
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td><strong>authorization_key</strong></td>
    <td><em>string</em></td>
    <td>autorizační klíč kontaktu</td>
    <td><code>"SeCr3t:T0k3n"</code></td>
  </tr>
  <tr>
    <td><strong>city</strong></td>
    <td><em>string</em></td>
    <td>město</td>
    <td><code>"Praha"</code></td>
  </tr>
  <tr>
    <td><strong>country</strong></td>
    <td><em>string</em></td>
    <td>kód státu</td>
    <td><code>"CZ"</code></td>
  </tr>
  <tr>
    <td><strong>email</strong></td>
    <td><em>string</em></td>
    <td>e-mail</td>
    <td><code>"info@kraxnet.cz"</code></td>
  </tr>
  <tr>
    <td><strong>fax</strong></td>
    <td><em>string</em></td>
    <td>fax</td>
    <td><code>420.2201992</code></td>
  </tr>
  <tr>
    <td><strong>first_name</strong></td>
    <td><em>string</em></td>
    <td>jméno</td>
    <td><code>"Jiří"</code></td>
  </tr>
  <tr>
    <td><strong>hide</strong></td>
    <td><em>string</em></td>
    <td>skryté údaje</td>
    <td><code>""</code></td>
  </tr>
  <tr>
    <td><strong>id</strong></td>
    <td><em>string</em></td>
    <td>identifikátor kontaktu</td>
    <td><code>"KRAXNET"</code></td>
  </tr>
  <tr>
    <td><strong>ident</strong></td>
    <td><em>string</em></td>
    <td>hodnota identifikátoru</td>
    <td><code>26460335</code></td>
  </tr>
  <tr>
    <td><strong>ident_type</strong></td>
    <td><em>string</em></td>
    <td>typ identifikátoru (OP,Pas,MPSV,IC,Datum narození)</td>
    <td><code>"IC"</code></td>
  </tr>
  <tr>
    <td><strong>last_name</strong></td>
    <td><em>string</em></td>
    <td>příjmení</td>
    <td><code>"Kubíček"</code></td>
  </tr>
  <tr>
    <td><strong>notify_email</strong></td>
    <td><em>string</em></td>
    <td>e-mail pro oznámení</td>
    <td><code>"notify@kraxnet.cz"</code></td>
  </tr>
  <tr>
    <td><strong>organization</strong></td>
    <td><em>string</em></td>
    <td>firma</td>
    <td><code>"KRAXNET s.r.o."</code></td>
  </tr>
  <tr>
    <td><strong>phone</strong></td>
    <td><em>string</em></td>
    <td>telefon</td>
    <td><code>420.220199201</code></td>
  </tr>
  <tr>
    <td><strong>state</strong></td>
    <td><em>string</em></td>
    <td>region</td>
    <td><code>""</code></td>
  </tr>
  <tr>
    <td><strong>street</strong></td>
    <td><em>string</em></td>
    <td>ulice, číslo popisné</td>
    <td><code>"Kamenická 26"</code></td>
  </tr>
  <tr>
    <td><strong>tld</strong></td>
    <td><em>string</em></td>
    <td>doména nejvyššího řádu (TLD)</td>
    <td><code>"cz"</code></td>
  </tr>
  <tr>
    <td><strong>vat</strong></td>
    <td><em>string</em></td>
    <td>DIČ</td>
    <td><code>"CZ26460335"</code></td>
  </tr>
  <tr>
    <td><strong>zip</strong></td>
    <td><em>string</em></td>
    <td>poštovní směrovací číslo</td>
    <td><code>17000</code></td>
  </tr>
</table>


#### Curl Example
```term
$ curl -n -X POST https://api.hello.com/contacts/update
-H "Content-Type: application/json" \
-d '{"tld":"cz","id":"KRAXNET","organization":"KRAXNET s.r.o.","first_name":"Jiří","last_name":"Kubíček","email":"info@kraxnet.cz","phone":420.220199201,"fax":420.2201992,"ident_type":"IC","ident":26460335,"street":"Kamenická 26","city":"Praha","zip":17000,"country":"CZ","state":"","vat":"CZ26460335","authorization_key":"SeCr3t:T0k3n","notify_email":"notify@kraxnet.cz","hide":""}'
```


#### Response Example
```
HTTP/1.1 200 OK
```
```json
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "registry_object_name": "kraxnet.cz",
  "object_type": "domain",
  "request_type": "check",
  "content": "{}",
  "status": "successful"
}
```

### Contact Delete
Služba pro zrušení kontaktu, který není navázán na žádný objekt (doména, nsset, keyset).

```
POST /contacts/delete
```

#### Optional Parameters
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td><strong>id</strong></td>
    <td><em>string</em></td>
    <td>identifikátor kontaktu</td>
    <td><code>"KRAXNET"</code></td>
  </tr>
</table>


#### Curl Example
```term
$ curl -n -X POST https://api.hello.com/contacts/delete
-H "Content-Type: application/json" \
-d '{"id":"KRAXNET"}'
```


#### Response Example
```
HTTP/1.1 200 OK
```
```json
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "registry_object_name": "kraxnet.cz",
  "object_type": "domain",
  "request_type": "check",
  "content": "{}",
  "status": "successful"
}
```


## Request
FIXME

### Attributes
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td><strong>content</strong></td>
    <td><em>string</em></td>
    <td>Obsah požadavku</td>
    <td><code>"{}"</code></td>
  </tr>
  <tr>
    <td><strong>id</strong></td>
    <td><em>uuid</em></td>
    <td>unique identifier of request</td>
    <td><code>"01234567-89ab-cdef-0123-456789abcdef"</code></td>
  </tr>
  <tr>
    <td><strong>object_type</strong></td>
    <td><em>string</em></td>
    <td>Typ objektu v registru</td>
    <td><code>"domain"</code></td>
  </tr>
  <tr>
    <td><strong>registry_object_name</strong></td>
    <td><em>string</em></td>
    <td>Identifikátor objektu v registru</td>
    <td><code>"kraxnet.cz"</code></td>
  </tr>
  <tr>
    <td><strong>request_type</strong></td>
    <td><em>string</em></td>
    <td>Typ požadavku na práci s objektem</td>
    <td><code>"check"</code></td>
  </tr>
  <tr>
    <td><strong>status</strong></td>
    <td><em>string</em></td>
    <td>Stav zpracování požadavku</td>
    <td><code>"successful"</code></td>
  </tr>
</table>

### Request Info
Služba pro získání obsahu odeslaného požadavku.

```
GET /requests/{request_id}
```


#### Curl Example
```term
$ curl -n -X GET https://api.hello.com/requests/$REQUEST_ID
```


#### Response Example
```
HTTP/1.1 200 OK
```
```json
{
  "id": "01234567-89ab-cdef-0123-456789abcdef",
  "registry_object_name": "kraxnet.cz",
  "object_type": "domain",
  "request_type": "check",
  "content": "{}",
  "status": "successful"
}
```



