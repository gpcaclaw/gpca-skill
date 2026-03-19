# GPCA MCP Tools Reference

## Authentication & Registration
| Tool | Purpose | Params |
|------|---------|--------|
| `gpca_get_captcha` | Get captcha image for registration | — |
| `gpca_register` | Register new account (sends email code) | `email`, `username`, `password`, `r_password`, `validate_code`, `recommender_code?` |
| `gpca_finish_register` | Complete registration with email code | `register_id`, `verify_code` |
| `gpca_login` | Start login (sends email code) | `email`, `password` |
| `gpca_verify_login` | Complete login with code | `code` |
| `gpca_send_reset_password_email` | Send account recovery code | `email` |
| `gpca_reset_password` | Reset access code with verification | `email`, `code`, `new_password` |
| `gpca_auth_status` | Check if authenticated | — |
| `gpca_get_user_info` | Get user profile | — |

## Card Management
| Tool | Purpose | Params |
|------|---------|--------|
| `gpca_list_cards` | List user's cards | — |
| `gpca_supported_cards` | Available card types | — |
| `gpca_order_virtual_card` | Apply for virtual card | `card_type_id` |
| `gpca_bind_card` | Bind a card | `card_id` |
| `gpca_activate_card` | Activate card | `card_id` |
| `gpca_freeze_card` | Freeze/unfreeze card | `card_id` |
| `gpca_change_pin` | Change card PIN | `card_id`, `old_pin`, `new_pin` |
| `gpca_reset_pin` | Reset card PIN | `card_id` |
| `gpca_get_cvv` | Get card security code | `card_id` |
| `gpca_card_transactions` | Card transaction history | `card_id`, `start_time?`, `end_time?` |

## Wallet
| Tool | Purpose | Params |
|------|---------|--------|
| `gpca_wallet_balance` | Wallet balance | — |
| `gpca_supported_chains` | Supported transfer networks | — |
| `gpca_deposit_address` | Wallet deposit address | `chain` |
| `gpca_bank_card_list` | Cards for deposit | — |
| `gpca_deposit_to_card` | Transfer funds to card | `card_id`, `amount` |
| `gpca_wallet_transactions` | Wallet history | `start_time`, `end_time?` |

## Identity Verification
| Tool | Purpose | Params |
|------|---------|--------|
| `gpca_check_kyc` | Verification status | — |
| `gpca_request_kyc` | Start Mastercard verification | `kyc_data` |
| `gpca_request_kyc_visa` | Start Visa verification | `kyc_data` |
| `gpca_submit_kyc` | Submit verification | `kyc_data` |
| `gpca_add_kyc_file` | Upload verification document | `kyc_data` |
| `gpca_reset_kyc` | Reset verification | — |

## Notifications & Support
| Tool | Purpose | Params |
|------|---------|--------|
| `gpca_notification_list` | System notifications | `page?` |
| `gpca_notification_detail` | Notification detail | `id` |
| `gpca_view_all_tickets` | List support tickets | — |
| `gpca_get_ticket_detail` | Ticket detail | `ticket_id` |
| `gpca_create_ticket` | Create support ticket | `title`, `content` |
| `gpca_reply_ticket` | Reply to ticket | `ticket_id`, `content` |
| `gpca_close_ticket` | Close ticket | `ticket_id` |

## Spending Limits
| Tool | Purpose | Params |
|------|---------|--------|
| `gpca_set_spending_limit` | Set spending limits | `per_transaction?`, `daily?`, `monthly?` |
| `gpca_get_spending_limits` | Get current limits | — |
| `gpca_spending_summary` | Spending records | `period?` |
| `gpca_remove_spending_limit` | Remove limits | `type` |
| `gpca_record_spending` | Record a purchase | `amount`, `description` |
