---
enablefeatureboxes: false
visible: true
sidebar:
    -
        route: /_partials/_three-easy-steps
    -
        route: /_partials/_state-licensure-requirements
    -
        route: /_partials/_state-medical-board-links
    -
        route: /_partials/_wise-words
content:
    items:
        - '@self.children'
    limit: 5
    order:
        by: date
        dir: desc
    pagination: true
    url_taxonomy_filters: true
---

