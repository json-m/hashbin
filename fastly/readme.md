### about

hashbin over fastly using only synthetic responses (no origin!)

using this you can run it for free on fastly.com with any developer account (400GB~?)


##### how-to

1. clone your config
2. add a domain or subdomain (preferred, ie. hb.zj.is)
3. go to vcl snippets, we're going to create 2
4. name this one `synthetic-router`
5. set within subroutine `vcl_recv`
6. paste the contents of `router.synth` in the fastly folder into the VCL box
7. change to your domain in the condition, then hit update
8. return to snippets, make another
9. name `965-bin`
10. within subroutine `vcl_error`
11. paste the contents of `hashbin.synth` in the fastly folder into the VCL box, hit update
12. hit the green activate button, your service should go live in less than 10seconds