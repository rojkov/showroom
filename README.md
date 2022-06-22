Envoy
=====

Compression framework for Envoy
-------------------------------

The design doc: https://docs.google.com/document/d/1Fsrjwu7B-gzWmqx-Ne5qVKNUqJK6eHPQ8O6WlgiFRXM/edit?ts=5dfcbb36#heading=h.gjdgxs

The first PR introducing the new compression framework in Envoy:
https://github.com/envoyproxy/envoy/pull/7057

A follow-up which activates the new framework:
https://github.com/envoyproxy/envoy/pull/10306

Actually make the framework visible for end users:
https://github.com/envoyproxy/envoy/pull/10553

Extend the framework to support request payloads:
https://github.com/envoyproxy/envoy/pull/14302

Add brotli compression in addition to gzip
https://github.com/envoyproxy/envoy/pull/12998

Performance fixes
-----------------

Fix for exponential growth of consumed memory in control plane
https://github.com/envoyproxy/envoy/pull/15013

Avoid quadratic time complexity in server initialization
https://github.com/envoyproxy/envoy/pull/15347

Examples of code reviews
------------------------

New socket implementation bypassing Linux kernel:
https://github.com/envoyproxy/envoy/pull/18149

https://github.com/envoyproxy/envoy/pull/17811

https://github.com/envoyproxy/envoy/pull/15967

Add zstd compressor and decompressor:
https://github.com/envoyproxy/envoy/pull/20434

Kubernetes
==========

A security fix in API-server to handle JSON-patches created by mutating webhooks correctly:
https://github.com/kubernetes/kubernetes/pull/64255

Not K8s per se, but a quick and dirty solution enabling placing AVX-heavy workloads on the same CPU cores for better performance (cri-resource manager is a proxy sitting between kubelet and a container runtime):
https://github.com/intel/cri-resource-manager/pull/61/files

systemd
=======

Add support for MulticastDNS server:
https://github.com/systemd/systemd/pull/4832

Add support for server-side DNS-SD in mDNS zones (used for Service Discovery in local networks, replaces Avahi):
https://github.com/systemd/systemd/pull/6993

Mozilla Firefox
===============

Turn GestureEventListener into Finite-state machine ([Ratio behind the change and discussion](https://bugzilla.mozilla.org/show_bug.cgi?id=985541)):
https://hg.mozilla.org/mozilla-central/rev/de2d3a740e06cdb3279cbb8e88cb63db62445ebe
