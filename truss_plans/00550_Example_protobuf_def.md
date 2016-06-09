
<style type="text/css">
#slides {
	font-size: 15px;
}
pre {
	font-size: 15px;
}

h2 {
font-size: 70px;
}

</style>

# HTTP Annotations example

	::protobuf hl_lines="1 5 7 8 15 16 21 23 24"
	import "google/api/annotations.proto";

	service CurrencyExchangeService {

  		/// Return a particular exchange rate for a currency
		rpc ExchangeRateGetRate(ExchangeRateGetRateRequest) returns (ExchangeRateGetRateResponse) {
			option (google.api.http) = {
				get: "/rate/{from_currency}/{to_currency}"
			};
		}

  		/// Convert an amount in one currency to another at an exchange rate
		rpc ExchangeRateConvert(ExchangeRateConvertRequest) returns (ExchangeRateConvertResponse) {
			option (google.api.http) = {
				post: "/convert"
				body: "rate"
			};
		}
	}

	/// Input request for ExchangeRateGetRate rpc method of CurrencyExchangeService
	message ExchangeRateGetRateRequest {
	  /// Input currency type
	  /// Must be ISO 4217 3 letter currency code
	  string from_currency = 1;
	  ...

