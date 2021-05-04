# can generate three types of row

    Code
      data_reference_index(pkg)
    Output
      pagetitle: Function reference
      rows:
      - title: A
        slug: section-a
        desc: ~
      - subtitle: B
        slug: section-b
        desc: ~
      - topics:
        - path: a.html
          aliases: a()
          title: A
          icon: ~
        - path: b.html
          aliases: b()
          title: B
          icon: ~
        - path: c.html
          aliases: c()
          title: C
          icon: ~
        - path: help.html
          aliases: '`?`()'
          title: D
          icon: ~
        names:
        - a
        - b
        - c
        - '?'
        row_has_icons: no
      has_icons: no
      
