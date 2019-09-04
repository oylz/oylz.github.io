I'm an architect focus on database processing and AI develop.

* history:
  * a global data synchronization solution, make sure final consistency
    * extract postgres changed records from WAL.
    * extract redis change data from AOF&RDB
    * use **vector clock time** to make sure the records are final consistency
    * extend sql command, just like **sync_insert**, **sync_delete** and **sync_update**, for the syncer to terminal.
    * extend redis command, just like **upvct**,**commitvct**,**syncupvct**,**synccommitvct**,**hsetex**,**hexpire** and so on.
  
  * [a face tracking implement](https://github.com/oylz/DS), base on deepsort\-\- Simple Online Realtime Tracking with a Deep Association Metric
  
  
* TODO: [gperftools](https://github.com/oylz/gperftools), [it's doc](https://oylz.github.io/gperftools/)


