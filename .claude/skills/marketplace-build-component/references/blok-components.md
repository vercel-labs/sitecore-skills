# Blok Component Catalog

All components are installed via `npx shadcn@latest add <url>` where the URL is `https://blok.sitecore.com/r/<name>.json`.

## Theme (install first)

| Component | Install Command |
|-----------|----------------|
| Blok Theme | `npx shadcn@latest add https://blok.sitecore.com/r/theme.json` |

## Layout & Structure

| Component | Install URL slug | Description |
|-----------|-----------------|-------------|
| Card | `card.json` | Container with header, content, footer |
| Separator | `separator.json` | Horizontal or vertical divider |
| Tabs | `tabs.json` | Tabbed content panels |
| Accordion | `accordion.json` | Collapsible content sections |
| Sheet | `sheet.json` | Side panel overlay |
| Dialog | `dialog.json` | Modal dialog |
| Drawer | `drawer.json` | Bottom drawer panel |
| Collapsible | `collapsible.json` | Toggle content visibility |
| Resizable | `resizable.json` | Resizable panels |
| ScrollArea | `scroll-area.json` | Custom scrollbar area |
| AspectRatio | `aspect-ratio.json` | Maintain aspect ratios |

## Forms & Input

| Component | Install URL slug | Description |
|-----------|-----------------|-------------|
| Button | `button.json` | Click actions, variants: default/destructive/outline/secondary/ghost/link |
| Input | `input.json` | Text input field |
| Textarea | `textarea.json` | Multi-line text input |
| Select | `select.json` | Dropdown selection |
| Checkbox | `checkbox.json` | Boolean toggle |
| RadioGroup | `radio-group.json` | Single selection from options |
| Switch | `switch.json` | Toggle switch |
| Slider | `slider.json` | Range slider |
| Label | `label.json` | Form field label |
| Form | `form.json` | Form with validation (react-hook-form + zod) |
| InputOTP | `input-otp.json` | One-time password input |
| DatePicker | `date-picker.json` | Date selection |
| Calendar | `calendar.json` | Calendar display |
| Combobox | `combobox.json` | Searchable select |
| Command | `command.json` | Command palette / search |
| Toggle | `toggle.json` | Toggle button |
| ToggleGroup | `toggle-group.json` | Group of toggle buttons |

## Data Display

| Component | Install URL slug | Description |
|-----------|-----------------|-------------|
| Table | `table.json` | Data table |
| DataTable | `data-table.json` | Full-featured data table (sorting, filtering, pagination) |
| Badge | `badge.json` | Status/category labels |
| Avatar | `avatar.json` | User avatar with fallback |
| Tooltip | `tooltip.json` | Hover tooltips |
| HoverCard | `hover-card.json` | Rich hover content |
| Popover | `popover.json` | Click-triggered popup |

## Feedback & Status

| Component | Install URL slug | Description |
|-----------|-----------------|-------------|
| Alert | `alert.json` | Alert messages (info/warning/error) |
| AlertDialog | `alert-dialog.json` | Confirmation dialog |
| Toast | `toast.json` | Toast notifications (also see SDK `app.toast`) |
| Skeleton | `skeleton.json` | Loading placeholder |
| Progress | `progress.json` | Progress bar |
| Sonner | `sonner.json` | Alternative toast library |

## Navigation

| Component | Install URL slug | Description |
|-----------|-----------------|-------------|
| NavigationMenu | `navigation-menu.json` | Top navigation |
| Menubar | `menubar.json` | Menu bar with dropdowns |
| DropdownMenu | `dropdown-menu.json` | Dropdown action menu |
| ContextMenu | `context-menu.json` | Right-click context menu |
| Breadcrumb | `breadcrumb.json` | Breadcrumb navigation |
| Pagination | `pagination.json` | Page navigation |
| Sidebar | `sidebar.json` | Sidebar navigation |

## Typography & Media

| Component | Install URL slug | Description |
|-----------|-----------------|-------------|
| Carousel | `carousel.json` | Image/content carousel |
| Chart | `chart.json` | Data visualization (recharts) |

## Installing Multiple Components

```bash
# Install several at once
npx shadcn@latest add https://blok.sitecore.com/r/card.json https://blok.sitecore.com/r/button.json https://blok.sitecore.com/r/input.json https://blok.sitecore.com/r/skeleton.json https://blok.sitecore.com/r/alert.json
```

## Usage Pattern

```tsx
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Skeleton } from "@/components/ui/skeleton";

export function MyWidget() {
  return (
    <Card>
      <CardHeader>
        <CardTitle>Widget Title</CardTitle>
      </CardHeader>
      <CardContent>
        <p>Content here</p>
        <Button>Action</Button>
      </CardContent>
    </Card>
  );
}
```
