# micronaut.security Skill

Use this skill to work with Norm module `micronaut.security` version 5. Use only declarations listed below.

## `micronaut.security`

Source: `JavaArrays.norm`

### `JavaStringArray`

```norm
class JavaStringArray
```

#### `JavaStringArray`

```norm
JavaStringArray(JavaStringArrayBindingToken token)
```

Parameters:

- `token`: `JavaStringArrayBindingToken`

#### `size`

```norm
Integer size()
```

Returns: `Integer`

#### `get`

```norm
String? get(Integer index)
```

Parameters:

- `index`: `Integer`

Returns: `String?`

#### `set`

```norm
Void set(Integer index, String? value)
```

Parameters:

- `index`: `Integer`
- `value`: `String?`

Returns: `Void`

### `javaStringArrayNew`

```norm
JavaStringArray javaStringArrayNew(Integer size)
```

Parameters:

- `size`: `Integer`

Returns: `JavaStringArray`

## `micronaut.security.annotation`

Source: `annotation/Secured.norm`

### `Secured`

```norm
annotation Secured implements TypeTarget, FunctionTarget, RuntimeRetention, InheritedAnnotation
```

#### `value`

```norm
List<String> value
```

Type: `List<String>`

## `micronaut.security.authentication`

Source: `authentication/Authentication.norm`

### `Authentication`

```norm
interface Authentication extends Principal, Serializable
```

#### `getAttributes`

```norm
JavaMap<String, Any>? getAttributes()
```

Returns: `JavaMap<String, Any>?`

#### `getRoles`

```norm
Collection<String>? getRoles()
```

Returns: `Collection<String>?`

#### `withRoles`

```norm
Authentication? withRoles(Collection<String>? arg0)
```

Parameters:

- `arg0`: `Collection<String>?`

Returns: `Authentication?`

#### `withRoles`

```norm
Authentication? withRoles(Collection<String>? arg0, Boolean arg1)
```

Parameters:

- `arg0`: `Collection<String>?`
- `arg1`: `Boolean`

Returns: `Authentication?`

#### `withUsername`

```norm
Authentication? withUsername(String? arg0)
```

Parameters:

- `arg0`: `String?`

Returns: `Authentication?`

### `authenticationBuild`

```norm
Authentication? authenticationBuild(String? arg0)
```

Parameters:

- `arg0`: `String?`

Returns: `Authentication?`

### `authenticationBuild`

```norm
Authentication? authenticationBuild(String? arg0, Collection<String>? arg1)
```

Parameters:

- `arg0`: `String?`
- `arg1`: `Collection<String>?`

Returns: `Authentication?`

## `micronaut.security.authentication`

Source: `authentication/AuthenticationRequest.norm`

### `AuthenticationRequest`

```norm
interface AuthenticationRequest<T, S>
```

Type parameters:

- `T`
- `S`

#### `getIdentity`

```norm
T? getIdentity()
```

Returns: `T?`

#### `getSecret`

```norm
S? getSecret()
```

Returns: `S?`

## `micronaut.security.authentication`

Source: `authentication/AuthenticationResponse.norm`

### `AuthenticationResponse`

```norm
interface AuthenticationResponse extends Serializable
```

#### `getAuthentication`

```norm
Optional<Authentication>? getAuthentication()
```

Returns: `Optional<Authentication>?`

#### `getMessage`

```norm
Optional<String>? getMessage()
```

Returns: `Optional<String>?`

#### `isAuthenticated`

```norm
Boolean isAuthenticated()
```

Returns: `Boolean`

### `authenticationResponseFailure`

```norm
AuthenticationResponse? authenticationResponseFailure()
```

Returns: `AuthenticationResponse?`

### `authenticationResponseFailure`

```norm
AuthenticationResponse? authenticationResponseFailure(String? arg0)
```

Parameters:

- `arg0`: `String?`

Returns: `AuthenticationResponse?`

### `authenticationResponseSuccess`

```norm
AuthenticationResponse? authenticationResponseSuccess(String? arg0)
```

Parameters:

- `arg0`: `String?`

Returns: `AuthenticationResponse?`

### `authenticationResponseSuccess`

```norm
AuthenticationResponse? authenticationResponseSuccess(String? arg0, Collection<String>? arg1)
```

Parameters:

- `arg0`: `String?`
- `arg1`: `Collection<String>?`

Returns: `AuthenticationResponse?`

## `micronaut.security.authentication.provider`

Source: `authentication/provider/AuthenticationProvider.norm`

### `AuthenticationProvider`

```norm
interface AuthenticationProvider<T, I, S> extends Ordered
```

Type parameters:

- `T`
- `I`
- `S`

#### `authenticate`

```norm
AuthenticationResponse? authenticate(AuthenticationRequest<I, S>? arg0)
```

Parameters:

- `arg0`: `AuthenticationRequest<I, S>?`

Returns: `AuthenticationResponse?`

#### `authenticate`

```norm
AuthenticationResponse? authenticate(T? arg0, AuthenticationRequest<I, S>? arg1)
```

Parameters:

- `arg0`: `T?`
- `arg1`: `AuthenticationRequest<I, S>?`

Returns: `AuthenticationResponse?`

## `micronaut.security.io.micronaut.core.order`

Source: `io/micronaut/core/order/Ordered.norm`

### `Ordered`

```norm
interface Ordered
```

## `micronaut.security.rules`

Source: `rules/SecurityRule.norm`

### `SecurityRule`

```norm
interface SecurityRule<T> extends Ordered
```

Type parameters:

- `T`

### `securityRuleFieldGetDenyAll`

```norm
String? securityRuleFieldGetDenyAll()
```

Returns: `String?`

### `securityRuleFieldGetIsAnonymous`

```norm
String? securityRuleFieldGetIsAnonymous()
```

Returns: `String?`

### `securityRuleFieldGetIsAuthenticated`

```norm
String? securityRuleFieldGetIsAuthenticated()
```

Returns: `String?`

## `micronaut.security.utils`

Source: `utils/SecurityService.norm`

### `SecurityService`

```norm
interface SecurityService
```

#### `getAuthentication`

```norm
Optional<Authentication>? getAuthentication()
```

Returns: `Optional<Authentication>?`

#### `hasRole`

```norm
Boolean hasRole(String? arg0)
```

Parameters:

- `arg0`: `String?`

Returns: `Boolean`

#### `isAuthenticated`

```norm
Boolean isAuthenticated()
```

Returns: `Boolean`

#### `username`

```norm
Optional<String>? username()
```

Returns: `Optional<String>?`

