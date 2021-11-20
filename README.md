# nestjs-clean-architecture

https://medium.com/@jonathan.pretre91/clean-architecture-with-nestjs-e089cef65045

**domain** contains the business code and its logic and has no outward dependency: nor on frameworks (NestJS in our case), nor on use_cases or infrastructure packages.

**usecases** is like a conductor. It will depend only on domain package to execute business logic. use_cases should not have any dependencies on infrastructure (including framework or npm module).

**infrastructure** contains all the technical details, configuration, implementations (database, web services, npm module, etc.), and must not contain any business logic. infrastructure has dependencies on domain, use_cases and frameworks.
