# Create new member

## Start a CCF network

```
. scripts/ccf/sandbox_local/up.sh
```
or
```
. scripts/ccf/az-cleanroom-aci/up.sh
```

These commands will also see an existing network if there is one and set all environment variables appropriately.

## Specify usage of AKV (optional)
```
export USE_AKV=true
```

## Create the member identity

```
. scripts/ccf/member/create.sh your_member_name
```

## Add the member

```
. scripts/ccf/member/add.sh $WORKSPACE/your_member_name_cert.pem
```

## Use the member for future proposals
```
. scripts/ccf/member/use.sh your_member_name
```

This script sets the appropriate envrionment variables such that any proposal done with `scripts/ccf/propose.sh` will use the member identity that was just created.
