# nG-SetEnvIf
An [nG Firewall](https://perishablepress.com/ng-firewall/) fork that replicates its functionality in `httpd` using `mod_setenvif` and tracks upstream release. The trade-off is between the efficiency [gained over `mod_rewrite`](https://httpd.apache.org/docs/2.4/rewrite/avoid.html) and [having to defer](https://www.webmasterworld.com/apache/4572958.htm) to any existing rewrite rules (eg for [permalink settings](https://glennmessersmith.com/pages/wphtaccess.html)).

The focus being on performance, no logging facility is provided in addition to `httpd`'s native logs. Backreference support has been removed to minimise memory footprint. **Use `mod_rewrite` for [testing](https://perishablepress.com/ng-firewall-logging/) before deploying nG-SetEnvIf.**  

&nbsp;  

**Use case:** [`httpd.conf`](https://httpd.apache.org/docs/2.4/howto/htaccess.html#when)  
**Requires:** `mod_setenvif`, `mod_authz_core`, `mod_log_config`  
**Documentation:** See discussions in [Using `mod_rewrite` to control access](https://httpd.apache.org/docs/2.4/rewrite/access.html)  
**Known issues & recipes:** See [Wiki](https://github.com/t18d/nG-SetEnvIf/wiki/Known-Issues)  
**Upstream version:** [8G](https://perishablepress.com/8g-firewall/), courtesy of Jeff Starr  
**Desideratum:** Porting to Cloudflare's free-tier WAF

<hr width="50%">

**Our Sponsor:** &nbsp;<img src="https://github.com/t18d/nG-SetEnvIf/assets/130416721/a2922b2d-a2b0-4b59-a1e2-07c8b8294693" width="200" />
