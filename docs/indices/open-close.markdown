---
layout: default
title: Connecting
menu_section: indices
menu_item: open-close
---


# Open/Close Index

The open and close index APIs allow to close an index, and later on opening it. A closed index has almost no overhead on the cluster (except for maintaining its metadata), and is blocked for read/write operations. A closed index can be opened which will then go through the normal recovery process.

## Open and close and index by name

	var r = this.ConnectedClient.CloseIndex(Test.Default.DefaultIndex);
	r = this.ConnectedClient.OpenIndex(Test.Default.DefaultIndex);


## Open and close default index

	var r = this.ConnectedClient.CloseIndex<ElasticSearchProject>();
	r = this.ConnectedClient.OpenIndex<ElasticSearchProject>();


