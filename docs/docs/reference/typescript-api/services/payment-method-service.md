---
title: "PaymentMethodService"
weight: 10
date: 2023-07-20T13:56:16.355Z
showtoc: true
generated: true
---
<!-- This file was generated from the Vendure source. Do not modify. Instead, re-run the "docs:build" script -->
import MemberInfo from '@site/src/components/MemberInfo';
import GenerationInfo from '@site/src/components/GenerationInfo';
import MemberDescription from '@site/src/components/MemberDescription';


## PaymentMethodService

<GenerationInfo sourceFile="packages/core/src/service/services/payment-method.service.ts" sourceLine="48" packageName="@vendure/core" />

Contains methods relating to <a href='/typescript-api/entities/payment-method#paymentmethod'>PaymentMethod</a> entities.

```ts title="Signature"
class PaymentMethodService {
  constructor(connection: TransactionalConnection, configService: ConfigService, roleService: RoleService, listQueryBuilder: ListQueryBuilder, eventBus: EventBus, configArgService: ConfigArgService, channelService: ChannelService, customFieldRelationService: CustomFieldRelationService, translatableSaver: TranslatableSaver, translator: TranslatorService)
  findAll(ctx: RequestContext, options?: ListQueryOptions<PaymentMethod>, relations: RelationPaths<PaymentMethod> = []) => Promise<PaginatedList<PaymentMethod>>;
  findOne(ctx: RequestContext, paymentMethodId: ID, relations: RelationPaths<PaymentMethod> = []) => Promise<PaymentMethod | undefined>;
  async create(ctx: RequestContext, input: CreatePaymentMethodInput) => Promise<PaymentMethod>;
  async update(ctx: RequestContext, input: UpdatePaymentMethodInput) => Promise<PaymentMethod>;
  async delete(ctx: RequestContext, paymentMethodId: ID, force: boolean = false) => Promise<DeletionResponse>;
  async assignPaymentMethodsToChannel(ctx: RequestContext, input: AssignPaymentMethodsToChannelInput) => Promise<Array<Translated<PaymentMethod>>>;
  async removePaymentMethodsFromChannel(ctx: RequestContext, input: RemovePaymentMethodsFromChannelInput) => Promise<Array<Translated<PaymentMethod>>>;
  getPaymentMethodEligibilityCheckers(ctx: RequestContext) => ConfigurableOperationDefinition[];
  getPaymentMethodHandlers(ctx: RequestContext) => ConfigurableOperationDefinition[];
  async getEligiblePaymentMethods(ctx: RequestContext, order: Order) => Promise<PaymentMethodQuote[]>;
  async getMethodAndOperations(ctx: RequestContext, method: string) => Promise<{
        paymentMethod: PaymentMethod;
        handler: PaymentMethodHandler;
        checker: PaymentMethodEligibilityChecker | null;
    }>;
}
```

### constructor

<MemberInfo kind="method" type="(connection: <a href='/typescript-api/data-access/transactional-connection#transactionalconnection'>TransactionalConnection</a>, configService: ConfigService, roleService: <a href='/typescript-api/services/role-service#roleservice'>RoleService</a>, listQueryBuilder: <a href='/typescript-api/data-access/list-query-builder#listquerybuilder'>ListQueryBuilder</a>, eventBus: <a href='/typescript-api/events/event-bus#eventbus'>EventBus</a>, configArgService: ConfigArgService, channelService: <a href='/typescript-api/services/channel-service#channelservice'>ChannelService</a>, customFieldRelationService: CustomFieldRelationService, translatableSaver: <a href='/typescript-api/service-helpers/translatable-saver#translatablesaver'>TranslatableSaver</a>, translator: TranslatorService) => PaymentMethodService"   />


### findAll

<MemberInfo kind="method" type="(ctx: <a href='/typescript-api/request/request-context#requestcontext'>RequestContext</a>, options?: ListQueryOptions&#60;<a href='/typescript-api/entities/payment-method#paymentmethod'>PaymentMethod</a>&#62;, relations: RelationPaths&#60;<a href='/typescript-api/entities/payment-method#paymentmethod'>PaymentMethod</a>&#62; = []) => Promise&#60;<a href='/typescript-api/common/paginated-list#paginatedlist'>PaginatedList</a>&#60;<a href='/typescript-api/entities/payment-method#paymentmethod'>PaymentMethod</a>&#62;&#62;"   />


### findOne

<MemberInfo kind="method" type="(ctx: <a href='/typescript-api/request/request-context#requestcontext'>RequestContext</a>, paymentMethodId: <a href='/typescript-api/common/id#id'>ID</a>, relations: RelationPaths&#60;<a href='/typescript-api/entities/payment-method#paymentmethod'>PaymentMethod</a>&#62; = []) => Promise&#60;<a href='/typescript-api/entities/payment-method#paymentmethod'>PaymentMethod</a> | undefined&#62;"   />


### create

<MemberInfo kind="method" type="(ctx: <a href='/typescript-api/request/request-context#requestcontext'>RequestContext</a>, input: CreatePaymentMethodInput) => Promise&#60;<a href='/typescript-api/entities/payment-method#paymentmethod'>PaymentMethod</a>&#62;"   />


### update

<MemberInfo kind="method" type="(ctx: <a href='/typescript-api/request/request-context#requestcontext'>RequestContext</a>, input: UpdatePaymentMethodInput) => Promise&#60;<a href='/typescript-api/entities/payment-method#paymentmethod'>PaymentMethod</a>&#62;"   />


### delete

<MemberInfo kind="method" type="(ctx: <a href='/typescript-api/request/request-context#requestcontext'>RequestContext</a>, paymentMethodId: <a href='/typescript-api/common/id#id'>ID</a>, force: boolean = false) => Promise&#60;DeletionResponse&#62;"   />


### assignPaymentMethodsToChannel

<MemberInfo kind="method" type="(ctx: <a href='/typescript-api/request/request-context#requestcontext'>RequestContext</a>, input: AssignPaymentMethodsToChannelInput) => Promise&#60;Array&#60;Translated&#60;<a href='/typescript-api/entities/payment-method#paymentmethod'>PaymentMethod</a>&#62;&#62;&#62;"   />


### removePaymentMethodsFromChannel

<MemberInfo kind="method" type="(ctx: <a href='/typescript-api/request/request-context#requestcontext'>RequestContext</a>, input: RemovePaymentMethodsFromChannelInput) => Promise&#60;Array&#60;Translated&#60;<a href='/typescript-api/entities/payment-method#paymentmethod'>PaymentMethod</a>&#62;&#62;&#62;"   />


### getPaymentMethodEligibilityCheckers

<MemberInfo kind="method" type="(ctx: <a href='/typescript-api/request/request-context#requestcontext'>RequestContext</a>) => ConfigurableOperationDefinition[]"   />


### getPaymentMethodHandlers

<MemberInfo kind="method" type="(ctx: <a href='/typescript-api/request/request-context#requestcontext'>RequestContext</a>) => ConfigurableOperationDefinition[]"   />


### getEligiblePaymentMethods

<MemberInfo kind="method" type="(ctx: <a href='/typescript-api/request/request-context#requestcontext'>RequestContext</a>, order: <a href='/typescript-api/entities/order#order'>Order</a>) => Promise&#60;PaymentMethodQuote[]&#62;"   />


### getMethodAndOperations

<MemberInfo kind="method" type="(ctx: <a href='/typescript-api/request/request-context#requestcontext'>RequestContext</a>, method: string) => Promise&#60;{

