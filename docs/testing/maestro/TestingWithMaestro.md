# Testing React Native Apps with Maestro

#### offical docs [here](https://maestro.mobile.dev/)

### Running tests in parallel

1. Create a .maestro folder in root
2. Structure subfolders by features:

```
.maestro
├── auth
│   ├── Login.yaml
│   └── Onboarding.yaml
├── checkout
│   ├── CheckoutWithCreditCard.yaml
│   ├── CheckoutWithGooglePay.yaml
│   └── CheckoutWithInvalidInfo.yaml
├── common
│   ├── OpenDeeplink.yaml
│   └── ScrollToSelected.yaml
└── search
    ├── FilterByCategory.yaml
    ├── Search.yaml
    ├── SearchHistory.yaml
    ├── SortByDate.yaml
    └── SortByPrice.yaml
```

3. Create config.yaml put it in root

```
flows:
  - auth/*
  - checkout/*
  - search/*
```

4.  Start as many simulators as you want. Make sure the app you want to test is installed and you expo development build is running.

5.  Run test tests with (Example with 3 simulators)

```
maestro test --shards 3 .maestro/
```

6. Smile!
