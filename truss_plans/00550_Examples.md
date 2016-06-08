
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

	#!protobuf
	service CurrencyExchangeService {
		rpc ExchangeRateGetRate(ExchangeRateGetRateRequest) returns (ExchangeRateGetRateResponse) {
			option (google.api.http) = {
				get: "/v1/rate"
			};
		}
		rpc ExchangeRateConvert(ExchangeRateConvertRequest) returns (ExchangeRateConvertResponse) {
			option (google.api.http) = {
				get: "/v1/convert"
			};
		}
		rpc Status(StatusRequest) returns (StatusResponse) {
			option (google.api.http) = {
				get: "/v1/status"
			};
		}
		rpc Ping(PingRequest) returns (PingResponse) {
			option (google.api.http) = {
				get: "/v1/ping"
			};
		}
	}

