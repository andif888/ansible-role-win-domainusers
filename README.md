# ansible-role-win-domainusers

Role to add, remove users, groups and memberships to an existing AD domain

## Table of content

- [Default Variables](#default-variables)
  - [win_domain_group_memberships_add_list](#win_domain_group_memberships_add_list)
  - [win_domain_group_memberships_remove_list](#win_domain_group_memberships_remove_list)
  - [win_domain_groups_add_list](#win_domain_groups_add_list)
  - [win_domain_groups_remove_list](#win_domain_groups_remove_list)
  - [win_domain_users_add_list](#win_domain_users_add_list)
  - [win_domain_users_remove_list](#win_domain_users_remove_list)
  - [win_path_seperator](#win_path_seperator)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Default Variables

### win_domain_group_memberships_add_list

A list of memberships to add

#### Default value

```YAML
win_domain_group_memberships_add_list: []
```

#### Example usage

```YAML
win_domain_group_memberships_add_list:
  - name: "group1"
    members:
      - "user1"
      - "user2"
  - name: "group2"
    members:
      - "user3"
      - "user4"
```

### win_domain_group_memberships_remove_list

a list of memberships to remove

#### Default value

```YAML
win_domain_group_memberships_remove_list: []
```

#### Example usage

```YAML
win_domain_group_memberships_remove_list:
  - name: "group1"
    members:
      - "user1"
      - "user2"
  - name: "group2"
    members:
      - "user3"
      - "user4"
```

### win_domain_groups_add_list

Specify a list of local groups to be added

#### Default value

```YAML
win_domain_groups_add_list: []
```

#### Example usage

```YAML
win_domain_groups_add_list:
 - { name: "group1", category: "security", description: "desc1", displayname: "group1" }
 - { name: "group2", description: "desc2" }
 - { name: "group3", description: "desc3" }
```

### win_domain_groups_remove_list

Specify a list of local groups to be removed

#### Default value

```YAML
win_domain_groups_remove_list: []
```

#### Example usage

```YAML
win_domain_groups_remove_list:
 - "group1"
 - "group2"
 - "group3"
```

### win_domain_users_add_list

Specify a list of local users to be added

#### Default value

```YAML
win_domain_users_add_list: []
```

#### Example usage

```YAML
win_domain_users_add_list:
 - { name: "user1", description: "desc1", fullname: "", password: "", password_expired: false, password_never_expires: false }
 - { name: "user2", description: "desc2" }
 - { name: "user3", description: "desc3" }
```

### win_domain_users_remove_list

Specify a list of local users to be removed

#### Default value

```YAML
win_domain_users_remove_list: []
```

#### Example usage

```YAML
win_domain_users_remove_list:
 - "user1"
 - "user2"
 - "user3"
```

### win_path_seperator

backslash in variable for easy handling

#### Default value

```YAML
win_path_seperator: \
```



## Dependencies

None.

## License

license (GPL-2.0-or-later, MIT, etc)

## Author

andif888
