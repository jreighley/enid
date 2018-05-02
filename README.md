# enid
Datascript adapter for the BCH blockchain. 

# rationale
If we use the expanded BCH Op code to store :entity :attribute :value and :validity we can create a datomic style datastore that would allow for storage of data for the life of the BCH chain very inexpesively.

Security could be built in rather easily as transactions originating address would be filtered for authorized originators, and transactions from other addresses would be ignored or consumed as tips.

# to do
* Find a good library for reading and writing BCH transactions

* Decide a general schema for how to best devide the 220 bytes of the op code 

* Write code to build samples.

* Consider security options. I suspect this can be done within the database itself -- The original depositor is the admin, and can authorize additional addresses to append transactions.  In theory you chold chard the DB to one entity per address and build a tree of DB's with different permissions.

# inspiration
* http://memo.cash
* https://github.com/tonsky/datascript
* http://datomic.com
