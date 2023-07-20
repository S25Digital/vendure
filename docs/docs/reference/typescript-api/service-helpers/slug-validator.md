---
title: "SlugValidator"
weight: 10
date: 2023-07-20T13:56:15.941Z
showtoc: true
generated: true
---
<!-- This file was generated from the Vendure source. Do not modify. Instead, re-run the "docs:build" script -->
import MemberInfo from '@site/src/components/MemberInfo';
import GenerationInfo from '@site/src/components/GenerationInfo';
import MemberDescription from '@site/src/components/MemberDescription';


## SlugValidator

<GenerationInfo sourceFile="packages/core/src/service/helpers/slug-validator/slug-validator.ts" sourceLine="44" packageName="@vendure/core" />

Used to validate slugs to ensure they are URL-safe and unique. Designed to be used with translatable
entities such as <a href='/typescript-api/entities/product#product'>Product</a> and <a href='/typescript-api/entities/collection#collection'>Collection</a>.

```ts title="Signature"
class SlugValidator {
  constructor(connection: TransactionalConnection)
  async validateSlugs(ctx: RequestContext, input: T, translationEntity: Type<E>) => Promise<T>;
}
```

### constructor

<MemberInfo kind="method" type="(connection: <a href='/typescript-api/data-access/transactional-connection#transactionalconnection'>TransactionalConnection</a>) => SlugValidator"   />


### validateSlugs

<MemberInfo kind="method" type="(ctx: <a href='/typescript-api/request/request-context#requestcontext'>RequestContext</a>, input: T, translationEntity: Type&#60;E&#62;) => Promise&#60;T&#62;"   />




## InputWithSlug

<GenerationInfo sourceFile="packages/core/src/service/helpers/slug-validator/slug-validator.ts" sourceLine="16" packageName="@vendure/core" />



```ts title="Signature"
type InputWithSlug = {
  id?: ID | null;
  translations?: Array<{
        id?: ID | null;
        languageCode: LanguageCode;
        slug?: string | null;
    }> | null;
}
```
## Members


### id

<MemberInfo kind="property" type="<a href='/typescript-api/common/id#id'>ID</a> | null"   />


### translations

<MemberInfo kind="property" type="Array&#60;{




## TranslationEntity

<GenerationInfo sourceFile="packages/core/src/service/helpers/slug-validator/slug-validator.ts" sourceLine="29" packageName="@vendure/core" />



```ts title="Signature"
type TranslationEntity = VendureEntity & {
    id: ID;
    languageCode: LanguageCode;
    slug: string;
    base: any;
}
```