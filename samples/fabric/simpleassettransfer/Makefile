run-vendor:
	go mod vendor
	cp -r ../../../common/protos-go/* vendor/github.com/hyperledger-labs/weaver-dlt-interoperability/common/protos-go/
	cp -r ../../../core/network/fabric-interop-cc/interfaces/asset-mgmt/* vendor/github.com/hyperledger-labs/weaver-dlt-interoperability/core/network/fabric-interop-cc/interfaces/asset-mgmt/
	cp -r ../../../core/network/fabric-interop-cc/libs/utils/* vendor/github.com/hyperledger-labs/weaver-dlt-interoperability/core/network/fabric-interop-cc/libs/utils/
	cp -r ../../../core/network/fabric-interop-cc/libs/testutils/* vendor/github.com/hyperledger-labs/weaver-dlt-interoperability/core/network/fabric-interop-cc/libs/testutils/

build-local: run-vendor
	go build -v .

build: clean-vendor
	go build -v .
	
test: clean-vendor
	go test -v .

clean-vendor:
	rm -rf vendor

clean: clean-vendor
	rm simpleassettransfer

test-local: run-vendor
	go test -v .


