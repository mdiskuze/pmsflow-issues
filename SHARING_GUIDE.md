# PMS Flow - Local Sharing Guide (.pmsshare)

This guide explains how local read-only sharing works in real life for:
- woman -> partner
- daughters -> mother (including multiple daughters)

The feature is fully local (no cloud account required).

---

## 1. What this sharing does

- Sender exports a **read-only snapshot** file: `.pmsshare`.
- Receiver imports that file into **Shared profiles**.
- Imported profile is separate from personal records.
- Receiver can view shared data, but cannot edit sender data.

---

## 2. Typical scenarios

### A) Woman shares to partner

Goal: Partner can see cycle context (next period estimate, basic overview), without editing her records.

Recommended export settings:
- Include symptoms: optional (ON if both agree)
- Include notes: usually OFF (privacy)

### B) Daughters share to mother

Goal: Mother can monitor multiple shared profiles in one app.

Recommended approach:
- Each daughter exports from her own device/profile.
- Mother imports each file into Shared profiles.
- Mother renames profiles clearly (e.g., "Anna", "Eli").

---

## 3. Sender steps (on daughter/woman phone)

1. Open `PMS Flow -> Shared profiles`.
2. Tap `Export shared snapshot (.pmsshare)`.
3. Optionally set:
   - profile alias,
   - include symptoms,
   - include notes.
4. Tap export button.
5. Android share sheet opens. Choose transfer method.

Common transfer options:
- Nearby Share / Quick Share (Android -> Android)
- Messaging app attachment (WhatsApp, Signal, Telegram)
- E-mail attachment
- Drive/Files upload and send link manually
- Bluetooth file transfer (older devices)
- USB cable copy to computer, then to target device

---

## 4. Receiver steps (partner/mother phone)

1. Save the `.pmsshare` file locally (if received via chat/email).
2. Open `PMS Flow -> Shared profiles`.
3. Tap `Import shared snapshot (.pmsshare)`.
4. Pick the file.
5. Confirm import.
6. Open profile detail, rename if needed.
7. Optionally set relationship label (Partner / Daughter / Father / Family / Other).

---

## 5. Multiple daughter workflow

Recommended setup on mother device:

1. Import first daughter snapshot.
2. Rename profile immediately (e.g., "Daughter - Anna").
3. Repeat for other daughters.
4. Use relationship label for each profile (recommended).
5. Use filter in Shared profiles for quick search.
6. Choose sorting mode (updated/name/relationship) for your preferred overview.
7. Optionally enable/disable:
   - **Keep snapshot history**
     - OFF: new snapshot from same sender updates existing shared profile.
     - ON: each new snapshot is kept as separate history entry.

---

## 6. How file updates work

- Each sender has a stable sender ID in snapshots.
- If `Keep snapshot history` is OFF, importing a newer snapshot from same sender updates that profile.
- If ON, each import is stored as a new entry.

---

## 7. Android version notes

### Android 13+ (API 33+)
- Notification runtime permissions do not affect file sharing itself.
- File picking/import works through system document picker.
- Nearby Share / Quick Share usually available depending on device ecosystem.
- `.pmsshare` can also be opened directly in PMS from Files/Drive/share sheet (when PMS is selected).

### Android 10-12
- Standard share sheet + document picker behavior.
- Scoped storage rules still allow this flow because app uses content URIs.

### Android 8-9
- Still supported by PMS Flow (min SDK 26).
- Share targets may vary by OEM apps installed.
- If direct sharing is limited, fallback to email or USB transfer.

### OEM differences (Samsung/Xiaomi/etc.)
- Share sheet labels differ (`Quick Share`, `Nearby Share`, vendor file manager names).
- Some messaging apps compress/transform attachments less predictably; if import fails, resend via Files/Drive/email.

---

## 8. Privacy and safety recommendations

- Use `Include notes = OFF` unless explicitly agreed.
- For partner view, consider symptoms OFF if minimal sharing is preferred.
- Rename shared profiles to avoid confusion.
- Delete old shared profiles if no longer needed.
- Do not share snapshots in public channels/groups.

---

## 9. Troubleshooting

### "Invalid .pmsshare file"
- Ensure selected file has `.pmsshare` extension.
- Re-export and resend from sender app.

### "Checksum mismatch" / import rejected
- File was modified/corrupted during transfer.
- Ask sender to export again and share via different channel.

### Profile did not update as expected
- Check `Keep snapshot history` setting in Shared profiles.
- OFF updates existing sender profile; ON creates additional entries.

### Imported profile not visible
- Open `Shared profiles` from the bottom navigation.
- Use filter field or clear filter text.

### Wrong profile order in list
- Use the Sort button in Shared profiles and select the desired ordering.

---

## 10. Quick checklist for real-life use

- Sender exported `.pmsshare`
- Receiver imported using Share Snapshot format
- Shared profile appears in Shared profiles
- Profile renamed for clarity
- Relationship label set
- Preferred sort mode selected
- Keep history setting verified
- New snapshot import tested once (update or history mode)
